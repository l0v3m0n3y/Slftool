# Slftool
api for slftool.github.io Compact solution for Stadt Land Fluss in German
# main
```cpp
#include "Slftool.h"
#include <iostream>

int main() {
   Slftool api;

    auto data = api.get_slftool_data().then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    data.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
