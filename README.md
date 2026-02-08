# Commands
These are the four commands that are evaluated, you can run them locally. To solve the errors faster.
- Validate format
```bash
# Linux & Windows
elm-format src/ --validate
```
- Run checks
```bash
# Linux
elm-review --template jfmengels/elm-review-common/example --rules NoMissingTypeAnnotation,NoMissingTypeAnnotationInLetIn
# Windows Powershell
elm-review --template jfmengels/elm-review-common/example --rules "NoMissingTypeAnnotation,NoMissingTypeAnnotationInLetIn"
# Windows cmd
elm-review --template jfmengels/elm-review-common/example --rules NoMissingTypeAnnotation,NoMissingTypeAnnotationInLetIn
```
- Build
```bash
# Linux
elm make src/*
# Windows
elm make src/<file>.elm
```
- Run tests
```bash
# Linux & Windows
elm-test
```

## Prerequisites
- NodeJs
- Elm
- elm-test 
- elm-format
- elm-review

# Exercises
## Records exercises
1.0 Let's define a record for programming languages with:
- name : String
- releaseYear : Int
- currentVersion: String

1.1 Create a list with at least two programming languages       
1.2 Create a function "languageNames" that receives the list from point 1.1 and generates a String list with only the names eg:      
- Input : [{name="elm", releaseYear= 2012, currentVersion="0.19.1"},{name="javascript", releaseYear= 1995, currentVersion="ECMAScript 2025"}]  
- Output: ["elm", "javascript"]


## Records exercises
2.0. Let's define a record for user with:
- name : String
- uType : String     

2.1 Create a list of users (uType can be "Student" or "Professor")      
2.2 Create a function "onlyStudents" that receives the list from point 2.1 and generates a String list with only the name of the "Student" (professors names are returned as an empty string) eg:
- Input : [{name="Roberto", uType= "Student"}, {name="Mitsiu", uType="Professor"}]
- Output: ["Roberto", ""]

## Aliases exercise
3.0 Let's define a record for games aliased "Videogame":
- title : String
- releaseYear : Int
- available: Bool
- downloads: Int
- genres : List String

3.1 Create a list with at least two videogames       
3.2 Create a function "getVideogameGenres" that receives the list from point 1.2 and generates a List of List of strings with only the genres eg:      
- Input : [{title="Control", releaseYear=2019, ... genres=["Action", "Shooter"]}, {title="Ocarina of time", ... genres=["Action", "Adventure"]}]
- Output: [["Action", "Shooter"], ["Action", "Adventure"]]

## Html exercise
Let's define a record named "Computer" with:
- ram: String
- model: String
- brand: String
- screenSize: String

And create a variable "myLaptop" of type Computer
       

Finally, let's make a variable "main" that reduces to:
```html
<div>
  <h1>My laptop<h1>
  <div>
    <ul>
      <li>Ram: {{.ram myLaptop}}</li>
      <li>Modelo: {{.model myLaptop}}</li>
      <li>Marca: {{.brand myLaptop}}</li>
      <li>Pulgadas: {{.screenSize myLaptop}}</li>
    </ul>
  </div>
</div>
```

