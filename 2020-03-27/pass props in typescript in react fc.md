### pass props in typescript in react fc


[typescript-cheatsheets/react-typescript-cheatsheet: Cheatsheets for experienced React developers getting started with TypeScript](https://github.com/typescript-cheatsheets/react-typescript-cheatsheet "typescript-cheatsheets/react-typescript-cheatsheet: Cheatsheets for experienced React developers getting started with TypeScript")


 

```ts
const TesbihItem: React.FC<{tesbihTitle: string}> = ({tesbihTitle}) => {
    const [title, setTitle] = useState("no title");
    const [counter, setCounter] = useState(0);


    const init = async () => {
        try {
            setTitle(tesbihTitle);
            const storageTesbihData = await Storage.get({ key: `${moment().format("YYYY-DD-MM")}-${title}-data` });
            storageTesbihData.value ? setCounter(Number(storageTesbihData.value)) : setCounter(0);
        } catch(err) {
        }
    }

----
<TesbihItem tesbihTitle={item.name}/>
```
