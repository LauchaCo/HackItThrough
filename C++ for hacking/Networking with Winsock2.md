__Windows.h__ doesn't get along pretty well with __Winsock2.h__. So in order to use both of them in the same file you have to include them like this:

```cpp
#define WIN32_LEAN_AND_MEAN
#include <Winddows.h>
#include <WinSock2.h>
```

Besides this, you also have to make a call to WSAStartup() before doing anything with the sockets. This can be done with the following code:

```cpp
#include <winsock2.h>

{
    WSADATA wsaData;

    if (WSAStartup(MAKEWORD(2, 2), &wsaData) != 0) {
        fprintf(stderr, "WSAStartup failed.\n");
        exit(1);
    }

    if (LOBYTE(wsaData.wVersion) != 2 ||
        HIBYTE(wsaData.wVersion) != 2)
    {
        fprintf(stderr,"Version 2.2 of Winsock not available.\n");
        WSACleanup();
        exit(2);
    }
```

In addition, you have to also include an additional statement at the start that tells the compiler to link the Winsock library "ws2_32.lib":

```cpp
#pragma comment(lib, "Ws2_32.lib")
```

