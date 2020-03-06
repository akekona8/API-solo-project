# Learning Chinese with APIs

This was created during my time as a student at Code Chrysalis

<!-- Add image of database diagram (with relations) -->

## HSK Vocabulary Words (Learning Chinese with APIs)

This repository explores the use of a CRUD API used to store and manipulate vocabulary words from the Hanyu Shuiping Kaoshi, Chinese literary language examination.

### Database schema

    id: generated by increments
    level: integer
    hanzi: string
    pinyin: string
    translations: string

## API

### GET

"/"
retrieve an array of all vocab words stored in the database.

"/id=:id"
retrieve a single vocabulary object by unique id.

"/level=:level"
retrieve all vocabulary objects of a given level. Examination levels range from Level 1-6.

### POST

"/"
add a new post suppling an object (with no id):

    level: integer
    hanzi: string
    pinyin: string
    translations: string

### PUT

"/:id"
update one or more fields of an existing vocabulary object (searching by id):

    level: integer
    hanzi: string
    pinyin: string
    translations: string

### DELETE

"/:id"
delete a vocabulary object (searching by id).
