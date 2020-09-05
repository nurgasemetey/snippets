###  java add hours to date


[Add Hours To a Date In Java | Baeldung](https://www.baeldung.com/java-add-hours-date "Add Hours To a Date In Java | Baeldung")


 

```
Function<NewProject, String> func = x -> {
									if(x.getPresidencyApprovalDate() != null) {
										Date newDate = Date.from(x.getPresidencyApprovalDate().toInstant().plus(Duration.ofHours(3)));//no way this app will be international use
										SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
										return sdf.format(newDate);
									}
									return null;
								};
								setCustomFunction(func);
```
