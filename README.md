# clinic-database

## First query

```SELECT COUNT(*) FROM visits where animal_id = 4;```

### Solution:

Added index on the animal_id column in the visits table.

```CREATE INDEX animal_id ON visits (animal_id);```

### Before:

![Screen Shot 2021-10-28 at 10 03 50](https://user-images.githubusercontent.com/10905837/139215456-4bc447a3-b048-44f4-862f-dd8f708672ed.png)


### After:

![Screen Shot 2021-10-28 at 10 10 27](https://user-images.githubusercontent.com/10905837/139215485-13afb267-48de-4de6-a19c-cf5065e4e9a2.png)




