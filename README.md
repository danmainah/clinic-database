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


## Third query

```SELECT * FROM owners where email = 'owner_18327@mail.com';```

### Solution:

Added index on email column in the owners table.

```CREATE INDEX email_id ON owners (email);```

### Before:

![Screenshot (37)](https://user-images.githubusercontent.com/61408860/139221692-d3b3a1a1-dcd5-4e27-aca0-f084bd1aa0d1.png)


### After:
![Screenshot (39)](https://user-images.githubusercontent.com/61408860/139221817-ba930acc-4bad-4c38-a9cf-8ebd79307a74.png)




