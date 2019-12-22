###  Curl soap 





 

```
time curl --header "Content-Type: text/xml;charset=UTF-8" --data @request.xml  http://a05.arvento.com/dataservice/gpsprovider.asmx?WSDL -o test.xml

<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:arv="http://www.arvento.com/">
   <soap:Header/>
   <soap:Body>
      <arv:GetCsvData>
         <!--Optional:-->
         <arv:Username>kgmtraffic</arv:Username>
         <!--Optional:-->
         <arv:Password><![CDATA[dhtb!47dbs&3a]]></arv:Password>
      </arv:GetCsvData>
   </soap:Body>
</soap:Envelope>
```
