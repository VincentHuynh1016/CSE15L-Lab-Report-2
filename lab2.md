# Part 1 
## StringServer Code
<img width="463" alt="image" src="https://github.com/VincentHuynh1016/CSE15L-Lab-Report-2/assets/114731503/e1402298-00b3-47fc-a276-394b15ece22a">

## Test1
<img width="959" alt="image" src="https://github.com/VincentHuynh1016/CSE15L-Lab-Report-2/assets/114731503/ba135698-aedc-468b-bb5b-45376a46a92d">

**Which methods in your code are called?**
- `handleRequeset(URI url)` is called to handle the request
- `url.getPath()` is called to get the path of the URL
- `url.getQuery()` is called to extract the query part of the URL
- `split("=")` is called to split the query parameters
- `messages.append(...)` is called to add the message to the messages StringBuilder
- `messages.toString()` is called to return the updated content as the response

**What are the relevant arguments to those methods, and the values of any relevant fields of the class?**
- `handleRequest(URI url)`:
  - Argument = URI url, represents the URL of the request
  - Values of Relevant Field: messages and sequence
- `url.getPath()`:
  - No Arguments: operates on the url object
  - Values of Relevant Field: `/add-message`
-`url.getQuery()`:
  - No Arguments: operates on the url object
  - Values of Relevant Field: `s=Hello`
- `split("=")`:
  - No Arguments: operates on the result of `url.getQuery()`
  - It split the query at the equal sign, result in an array parameters
    - `parameters[0] is "s"`
    - `parameters[1] is "Hello"`
- `messages.append()`:
  - Argument: String values are appended to the `messages` StringBuilder. In this case the value `1.Hello/n` is appended
  - Value of `sequence` is incremented to 2 after this operation
- `messages.toString()`:
  - No Arguments: operates on the `messages` StringBuilder
  - Returns the content of the `messages` StringBuilder as a string

**How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.**
- `sequence` field:
  - Initially the `sequence` field has a value of 1
  - After processing the request, the `sequence` field is incremented by 1 to 2
 
## Test 2
<img width="960" alt="image" src="https://github.com/VincentHuynh1016/CSE15L-Lab-Report-2/assets/114731503/86face76-759d-47ed-a47f-2f07d0ed894c">

**Which methods in your code are called?**
- `handleRequeset(URI url)` is called to handle the request
- `url.getPath()` is called to get the path of the URL
- `url.getQuery()` is called to extract the query part of the URL
- `split("=")` is called to split the query parameters
- `messages.append(...)` is called to add the message to the messages StringBuilder
- `messages.toString()` is called to return the updated content as the response

**What are the relevant arguments to those methods, and the values of any relevant fields of the class?**
- `handleRequest(URI url)`:
  - Argument = URI url, represents the URL of the request: /add-message?s=How are you
  - Values of Relevant Field: messages: contains the previous message "1.Hello/n" and sequence: value of 2 from previous request
- `url.getPath()`:
  - No arguments: Operates on the url object
  - Value of the path is `/add-message`
-`url.getQuery()`:
  - No arguments: it operates on the url object
  - Value of the query is `s=How are you`
- `split("=")`:
  - No arguments: It operates on the result of url.getQuery()
  - It splits the query at the equal sign which results in an array parameters
    - `parameters[0] is "s"`
    - `parameters[1] is "How are you"`
- `messages.append()`:
  - Arguments: String values are appended to the `messages` StringBuilder. In this case the value `2.How are you/n` is appended where 2 is the current value of the sequence.
  - Value of `sequence` is incremented to 3 now
-`messages.toString()`:
  - No Arguments: Operates on the `messages` StringBuilder
  - Returns the updated content of the `messages` StringBuilder, which now contains both previous messages `1.Hello/n` and the new message `2.How are you/n`.

**How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.**
-`sequence` field:
  - Initially the `sequence` field had a vlaue of 2 (from the pervious request)
  - After the new request, the `sequence` field is incremented and is now 3. 

# Part 2

<img width="253" alt="image" src="https://github.com/VincentHuynh1016/CSE15L-Lab-Report-2/assets/114731503/64f8d3dc-ce06-4668-99bf-a5cf8211bf37">

<img width="190" alt="image" src="https://github.com/VincentHuynh1016/CSE15L-Lab-Report-2/assets/114731503/8296f4a5-6cc8-475e-a48b-61696db44552">

We can see that locally, the private key is `id_rsa`. 

<img width="283" alt="image" src="https://github.com/VincentHuynh1016/CSE15L-Lab-Report-2/assets/114731503/be48bb77-7101-418f-8f6d-4999594f96a3">

In my ieng6 I have used `ls` command to show the path where the public key is located which is, `/home/linux/ieng6/cs15lfa23/cs15lfa23jn/.ssh/authorized_keys`.

<img width="430" alt="image" src="https://github.com/VincentHuynh1016/CSE15L-Lab-Report-2/assets/114731503/4b6a4f52-abdd-4e60-b8ae-358af2a8d82e">

# Part 3

In the second week lab, I delved into URLs and servers. I gained insight into the inner working of remote servers and acquired the knowledge and skills to operate a remote server from my own device. Throughout the lab, I executed a variety of commands on the server, gaining a deeper understanding of the significance of queires and paths in the context of server interaction. 

In third wees lab I learned how to set up VSCode for remote server operations. Additionally, I honed my ability to create and manage directories. This lab helped me understand server management but also helped me learn valuable tools for web development and other IT-related tasks.

