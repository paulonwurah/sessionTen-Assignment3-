# sessionTen-Assignment3-

Input = sc.parallelize([“Acadgild is the best school of the moment”])

flattenInput = input.flatMap(lambda x: x.split(“  “))

mapInput = flattenInput.map(lambda x: x.length)

mapInput.count()

reduceFlattenedInput = mapInput.reduce(lambda (x,y): (x+y))

KeyValue= flattenInput.map(lambda x: (x,1))

reduceKeyValue  = keyValue.reduceByKey(lambda(x,y): (x+y))

reduceByKey.collect()
