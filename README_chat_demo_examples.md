Once Docker from $2.1 is generated...



## 1. Creating a 'chat' file from a plain LLM ask with no tools

```bash

docker compose run --rm cli llm ask -c chats/hello.chat "What is the capital of France?"
# >> The capital of France is Paris.  

docker compose run --rm cli llm ask -c chats/hello.chat "and its population?"
# >> The population of Paris is approximately 2.1 million people within the city limits. However, the larger metropolitan area of Paris, known as the Île-de-France region, has a population of over 12.2 million people.

# if you want to see the provenance

docker compose run --rm cli llm prov chats/hello.chat --plot chats/prov.svg

Or skip the renderer entirely — --dot writes the Graphviz source and needs no binary:

docker compose run --rm cli llm prov chats/hello.chat --dot chats/prov.dot
dot -Tsvg chats/prov.dot -o chats/prov.svg     # on the host, if you have graphviz there
```



## 2. 
