fs = require "fs"
{exec} = require "child_process"
{spawn} = require "child_process"

task "build", "Build from src/* to lib/*", ->
  fs.exists "lib", (exists) ->
    if exists
      compile()
    else
      fs.mkdir "lib", (err) ->
        unless err
          console.log "Created lib/"
          compile()

compile = () ->
  exec "coffee --compile --output lib/ src/", (err, stdout, stderr) ->
    throw err if err
    console.log "Built okay!"
    console.log "\n#{stdout+stderr}" if stdout or stderr
