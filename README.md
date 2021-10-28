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


## Second query

```SELECT * FROM visits where vet_id = 2;```

### Solution:

Added index on both the animal_id and vet_id columns in the visits table.

```CREATE INDEX vet_animal ON visits (vet_id, animal_id);```

### Before:

![Screen Shot 2021-10-28 at 10 21 31](https://user-images.githubusercontent.com/10905837/139218225-9f3aba11-8a40-4519-8ccd-7c5ea64189af.png)

### After:

![Screen Shot 2021-10-28 at 10 28 30](https://user-images.githubusercontent.com/10905837/139218257-ee95007b-ba21-4097-bfd5-e4194fb2c9ef.png)




