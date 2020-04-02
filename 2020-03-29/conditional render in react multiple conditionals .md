### conditional render in react multiple conditionals 


[reactjs - Can I use multiple booleans for conditional rendering in React? - Stack Overflow](https://stackoverflow.com/questions/47680692/can-i-use-multiple-booleans-for-conditional-rendering-in-react "reactjs - Can I use multiple booleans for conditional rendering in React? - Stack Overflow")


 

```js
il && ilce && semt ? (geographyData as any)[il][ilce][semt].map((item: any, index: number) => (
                                            <IonSelectOption value={item}>{item}</IonSelectOption>
                                        )) : <div></div>
```
