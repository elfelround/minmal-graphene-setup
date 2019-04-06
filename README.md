localhost/graphql


type query:

query {
  allIngredients {
    id
    name
  }
}



query 2 (relations):

query {
  allCategories {
    id
    name
    ingredients {
      id
      name
    }
  }
}


query 3 (list):

query {
  allIngredients {
    id
    name
    category {
      id
      name
    }
  }
}


query 4 (single objects):

query {
  category(id: 1) {
    name
  }
  anotherCategory: category(name: "Dairy") {
    ingredients {
      id
      name
    }
  }
}
