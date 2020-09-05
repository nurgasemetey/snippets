###  turkish plate regex


[plate_validate_regex.swift](https://gist.github.com/10Macit/6beab310d6d9a12d9e97ca75b7f9a5b2 "plate_validate_regex.swift")


 

```

# "Türkiye plaka kodu için regular expression Swift 4.2"
# "99 X 9999", "99 X 99999"
# "99 XX 999", "99 XX 9999"
# "99 XXX 99", "99 XXX 999"

# "boşluk karakterleri silme"
let plate = self.plateStr.replacingOccurrences(of: " ", with: "").localizedUppercase

public static func isValidPlate(candidate: String) -> Bool {
        let pattern = "(0[1-9]|[1-7][0-9]|8[01])(([A-Z])(\\d{4,5})|([A-Z]{2})(\\d{3,4})|([A-Z]{3})(\\d{2,3}))"
        let predicate = NSPredicate(format: "self MATCHES [c] %@", pattern)
        return predicate.evaluate(with: candidate)
}

isValidPlate(plate)
```
