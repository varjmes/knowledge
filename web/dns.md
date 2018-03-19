# What happens when you type google.co.uk into your address bar and hit enter?

This is a common question in technical interviews.

In it's simplest, or most cheeky: if you type google.co.uk and press enter... you end up at google.co.uk. Tada!

What interviews are really looking for is insights into your knowledge about http, dns and servers.

When you type google.co.uk into your address bar and hit enter, you begin a request. google.co.uk is just an alias for an IP address, so a request is sent asking for an IP matching that URL.

If we're lucky, then your browser already has that link cached, "oh I know where this goes!". Failing that, maybe your Operating System knows where to go? Failing that, your Router, and failing _that_, your ISP (internet service provider).

If none of these entities have this cached, then it's time to talk to DNS servers. We'll send out a request with what we're looking for and keep bouncing around DNS servers until we get a hit.

Once we have the IP address we're looking for, we'll make a request to the server associated with that IP. Usually this will be a GET request for something as simple as trying to get a website, but it could also be POST, PUT, DELETE if we're making API calls or submitting a form.

The server will acknowledge the GET request and start transferring data back to you. For a GET request to google.co.uk this will result in an HTTP response that contains the data of the web page.

The browser will process this response and parse & render the HTML of the web page. Request complete!