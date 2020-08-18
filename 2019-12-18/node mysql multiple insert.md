### node mysql multiple insert







```js
        var vectorsTransformed = _.map(vectors, (vector) => {
            return `('${vector._id}', ST_GeomFromText('${geometry}'), ${speed})`;
        });
        // console.log(vectorsTransformed);
        client.close();
        console.log("mysql connected");
        const statement = 'INSERT INTO `tkm_geoserver_entities`.`bluesense_vector`(`id`, `geometry`, `speed`) VALUES '+ vectorsTransformed.slice(2).join(',') + ';';
        console.log(statement);
        const [results, fields] = await mysqlCon.execute(
            statement
        );
```
