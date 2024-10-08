Open Postman or navigate to localhost:4000 on browser and add the following in to the request . 

# Example to get all the games 
{
    games{
        id
        title
        platform
    }
}

# Example to get greeting " Hello World"
{
    greeting
}

# Example to get game with id 2 values 
{
    game(id:2){
        id
        title
        platform
    }
}

# Example to get all the authors 
{
    authors {
        id
        name
        verified
    }
}

# Example to get author with id 2
{
    author(id:2)
    {
        id
        name
        verified
    }
}

# Example to get all the reviews 
{
    reviews
    {
        id
        content
        author
        {
            id
            name
            verified
        }
        game
        {
            id
            title
            platform
        }
    }
}

# Example to get review based on ID
{
    review(id:1)
    {
        id
        content
        author{
        id
        name
        verified
    }
}  


# Example of mutation create
mutation {
    createGame(title:"Name Game 1",platform:["erer", "asdsa"])
}

# Example of mutation delete
mutation {
    deleteGame(id : 5505)
}

# Example of mutation update
mutation {
    updateGame(id: 1,title:"Name Game 1",platform:["erer", "asdsa"])
}

# Example of get after mutation
{
   
    game(id:1){
        id
        title
        platform
    }
}
