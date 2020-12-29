### python nodejs subprocess


[Python and Nodejs with subprocess](https://gist.github.com/webstory/bbd395911a93766c3168dae0c2800841 "Python and Nodejs with subprocess")




```
'use strict'

const http = require('http')

process.stdin.setEncoding('utf-8')
process.stdout.setEncoding('utf-8')
process.stdin.on('readable', () => {
  const content = process.stdin.read()
  if(!!content) {
    http.get(content, (res) => {
      if(res.statusCode >= 200 && res.statusCode < 400) {
        let body = ''

        res.on('data', (d) => body += d)
        res.on('end', () => console.log(body))
      } else {
        console.error(`[${res.statusCode}] ${res.statusMessage}`)
      }
    })
  }
})


----

def match(options):
    p = subprocess.Popen(['node', 'index.js'], stdin=subprocess.PIPE, stdout=subprocess.PIPE)
    data = json.dumps(options)
    response = p.communicate(data.encode())[0]
    # print(response)
    try: 
        as_json = json.loads(response)
        if as_json["status"]:
            print("matched")
            return as_json["response"]
        print("not matched")
        return False
    except Exception as e:
        print("error occured", e)
        return False
```
