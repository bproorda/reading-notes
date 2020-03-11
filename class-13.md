[Home](README.md)

# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS
- **Intro**
- long standing problem of web apps is storage
- started with cookies, but they have three big downsides
  - every HTTP includes cookies, bogs down the computer
  - send unencrypted data over internet
  - limited to 4kb, enough to slow down connection, but not to be very useful
- what is needed: lots of storage space, on the client side, persists beyond page refresh, is not transmitted to server
- **Introducting HTML5 Storage**
- HTML5 storage is a way for web pages to store key/values pairs locally.
- like cookies, they persist, but unlike cookies are not transmitted to server
- implemented natively in browser, not a browser plugin
- you'll access HTML5 storage using localStorage object on the global window object
-  ``` 
     ↶ check for HTML5 Storage

    function supports_html5_storage() {
    try {
        return 'localStorage' in window && window['localStorage'] !== null;
    } catch (e) {
        return false;
     }
    }
    Instead of writing this function yourself, you can use Modernizr to detect support for HTML5 Storage.

    if (Modernizr.localstorage) {
    // window.localStorage is available!
    } else {
    // no native support for HTML5 storage :(
    // maybe try dojox.storage or a third-party solution
    }
  ```
- **Using HTML5**
- key is stored as a string, call the key brings up the value attached to that key
- data type can be any of the js data types, but will be stored as a string
  - use parseInt or parseFloat as needed
- use square brackets, such as ` localStorage['keyword']
-  removing value from given key 
- ```
    interface Storage {
    deleter void removeItem(in DOMString key);
    void clear();
    };
 ```
 - 
 -  getting the totatl number of values in local storage
      ``` 
       interface Storage {
       readonly attribute unsigned long length;
       getter DOMString key(in unsigned long index);
       };
      ```

- **TRACKING CHANGES TO THE HTML5 STORAGE AREA**
- you can trap the storage event to track of when storage area changes
- store even is fired whenever setitem, getitem, removeitem or clear is called and local storage actually changes
