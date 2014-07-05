{exec} = require "child_process"
{spawn} = require "child_process"

task "build", "Build from src/* to lib/*", ->
  exec "coffee --compile --output lib/ src/", (err, stdout, stderr) ->
    throw err if err
    console.log "Built okay!"
    console.log "\n#{stdout+stderr}" if stdout or stderr

