After logging in to the forum as the user m0th3r_5up3r10r, we went to the general forum and submitted a post.
In the message of the post, we inserted an anchor tag with the link as the IP:PORT to a listening port that was established which contains the the exploit script to read all the cookies using an XmlHttpRequest

Now we have a service listening on port XXXX on localhost (nc -l -v IP PORT)

When the admin clicks on the link present in the post, we received the HTTP request on our service that reveals the session of the admin
We copied this session and replaced our user session with this new value and set it.

After setting the admin session and reloading the page we were successfully logged in as the admin.
Now inspecting the source of the forum page revealed the next secret at the bottom of the page source.

Note: This is not the only way to perform an XSS exploit. This is the one that was more convenient as per the situation.
