###  java sort list by field property


[java - How to sort List of objects by some property - Stack Overflow](https://stackoverflow.com/questions/5805602/how-to-sort-list-of-objects-by-some-property "java - How to sort List of objects by some property - Stack Overflow")


 

```
List<Pair<Integer, Integer>> startOfMinutePlanPairs = new ArrayList<>();
                        for(PlanTime planTime: planTimes) {
                            String startTime = planTime.getStartTime();
                            String[] splitStartTime = startTime.split(":");
                            Integer minuteOfDay = Integer.parseInt(splitStartTime[0])*60 + Integer.parseInt(splitStartTime[1]);
                            startOfMinutePlanPairs.add(new MutablePair<>(minuteOfDay, planTime.getId()));
                        }
                        Collections.sort(startOfMinutePlanPairs, new Comparator<Pair<Integer, Integer>>() {
                            @Override
                            public int compare(Pair<Integer, Integer> t1, Pair<Integer, Integer> t2) {
                                return t1.getKey().compareTo(t2.getKey());
                            }
                        });


---

Collections.sort(startOfMinutePlanPairs, new Comparator<Pair<Integer, Integer>>() {
                            @Override
                            public int compare(Pair<Integer, Integer> t1, Pair<Integer, Integer> t2) {
                                return t1.getKey().compareTo(t2.getKey());
                            }
                        });
```
