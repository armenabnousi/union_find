#Union Find
This is an implementation of union_find algorithm.</br>
To compute the connected components of a network you can pass in the network as a collection of nodes with their neighbors as std::vector<std::set<std::string>>* to the function `run_connected_component`. This function returns, as function''s output argument, the pointer to and std::unordered_set where the key is the name of the smallest node in the component (alphabetically smallest name), and the value is a vector of names of all the nodes present in that component.</br>
Todo: change std::set to a template type that will allow for accepting more efficient data structures as well.</br>
</br>
**Usage:**</br>
```c++
//edges: 1 <-> 2, 1 <-> 3, 4 <-> 5
//generating the example network:
std::vector<std::set<std::string>> neighbors_list;
std::string neighbors1[] = {"n1", "n2", "n3"};
neighbors_list.push_back (std::set<std::string>(neighbors1, neighbors1 + 3));
std::string neighbors2[] = {"n1", "n2"};
neighbors_list.push_back (std::set<std::string>(neighbors2, neighbors2 + 2));
std::string neighbors3[] = {"n1", "n3"};
neighbors_list.push_back (std::set<std::string>(neighbors3, neighbors3 + 2));
std::string neighbors4[] = {"n4", "n5"};
neighbors_list.push_back (std::set<std::string>(neighbors4, neighbors4 + 2));
neighbors_list.push_back (std::set<std::String>(neighbots4, neighbors4 + 2));

//computing the connected components:
UnionFind ufo();
std::unordered_set<std::string, std::vector<std::string>>* connected_components;
ufo.run_connected_component(&neighbors_list, &connected_components);

//resulting connected components: <n1, [n1, n2, n3]>, <n4, [n4, n5]>
```
