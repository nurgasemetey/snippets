###  useeffect async react


[javascript - React Hook Warnings for async function in useEffect: useEffect function must return a cleanup function or nothing - Stack Overflow](https://stackoverflow.com/questions/53332321/react-hook-warnings-for-async-function-in-useeffect-useeffect-function-must-ret "javascript - React Hook Warnings for async function in useEffect: useEffect function must return a cleanup function or nothing - Stack Overflow")


 

```js
function Example() {
  const [data, dataSet] = useState<any>(null)

  useEffect(() => {
    async function fetchMyAPI() {
      let response = await fetch('api/data')
      response = await response.json()
      dataSet(response)
    }

    fetchMyAPI()
  }, [])

  return <div>{JSON.stringify(data)}</div>
}
```
