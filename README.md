# GitHub_Simulation
GitHub Application in Cpp
GUI SCREENSHOTS
 


 

The provided C++ code implements essential data structures and functionalities for a GitHub-like application. It includes implementations of linked lists for managing files and commits within repositories, as well as a binary search tree for organizing repositories. File I/O operations are utilized to persist repository data, while balanced binary search tree operations ensure efficient retrieval and manipulation of repositories. This foundational code lays the groundwork for further development of a comprehensive version control system, although additional features such as user authentication and a graphical user interface would be necessary for a complete GitHub application.

1. Linked List Implementation:
   - >This class implements a basic linked list data structure.
   -> Functionalities include inserting a node (Insert()), deleting a node (Delete()), getting the node count (getNodeCount()), and retrieving data at a specific index (getDataAt()).

2. Binary Search Tree Implementation (Node and Repository_Manager classes):
   The “Node”struct represents a node in the binary search tree. Each node contains information about a repository, including its name, whether it's private or not, pointers to left and right children, and pointers to linked lists for files and commits associated with the repository.
   The “Repository_Manager” class manages the binary search tree of repositories. It provides functionalities for creating repositories, inserting files and commit messages into repositories, loading data from a file, saving data to a file, searching for repositories, and getting a list of repositories.

3. File I/O:
   The application reads and writes data to files to persist repository information. It uses file streams (fstream) to read from and write to files.
   -Data for repositories, including repository names, file names, commit messages, and privacy status, are stored in a file with the format <Owner>_repo.csv.

4. Balanced Binary Search Tree Operations:
   - >The `Repository_Manager` class implements functions to maintain the balance of the binary search tree by performing rotations (`rightRotate()` and `leftRotate()`) when necessary during insertion and deletion operations.
   - >These rotations ensure that the binary search tree remains balanced, which helps maintain efficient search and retrieval operations.

5. Other Operations:
   The code includes functions for setting the privacy status of repositories (`setPrivate()`), searching for repositories (`searchRepo()`), retrieving a repository by name (`getRepo()`), and getting a list of repositories (`getRepoList()`).
    Additionally, there are functions for inserting files and commit messages into repositories (`insertFile()` and `insertCommitMsg()`), as well as for loading and saving repository data from/to files (`loadData()` and `SaveData()`).
6. Memory Management:
    Ensure proper memory management, especially in the destructor of `Repository_Manager`, to avoid memory leaks. You're allocating memory dynamically for `Node` objects, so make sure to deallocate this memory when appropriate.
    Consider implementing copy constructors and copy assignment operators to properly handle copying of objects containing dynamically allocated memory.
7. Error Handling:
   - When performing operations like inserting a file or commit message into a repository, ensure that the repository exists before attempting to modify it. If the repository doesn't exist, handle this scenario gracefully, perhaps by returning an error code or throwing an exception.

8. Function Naming and Documentation:
   Be consistent with function naming conventions and ensure that function names are descriptive of their purpose.
   Consider adding comments or documentation to clarify the purpose and behavior of each function, especially for complex operations or algorithms.

9. Testing:
   - Thoroughly testr code with various scenarios, including edge cases such as empty repositories, non-existent repositories, and large datasets, to ensure correctness and robustness.

