---
layout: post
title:  "Cloudflare and SSL"
date:   2018-03-05 21:29:00 -0700
categories: security
excerpt: "Setting up a free SSL Certificate on personal websites - 1 hour challenge + how-to guide"
---

This week's one hour challenge involved getting a free SSL certificate for my personal website.

**Why SSL?**

I wanted one of those little green locks with the word "Secure" next to my url. I felt like this would legitimize my website and I am expanding it to include a blog and static resources like presentation slides. I also been considering refactoring it to use a frontend framework like React, Preact, or Vue.js.

Here is my little green lock:
![SSL Screenshot]({{ "/assets/ssl_screenshot.jpg" | absolute_url }})

Getting an SSL Certificate felt like a good first step in this journey. After finding the right tool for the job, Cloudflare (it was recommended by a friend; I floundered for a few days before connecting with this friend), the set up was quick and easy.

**Technology:**
- Site is hosted on [Github Pages](https://pages.github.com/)
- Domain purchased on mydomain.com
- [Cloudflare](https://www.cloudflare.com/) provided the SSL certificate

**How I got set up:**
1. Create a free account with Cloudflare
2. Add a site to your Cloudflare account by entering the domain url
3. Log into  domain registrar, select the domain.
4. Click on DNS to modify NS Record
5. Change the two "Points To:" records from ns1.nameserver.com (or ns2.nameserver.com or something of this nature) to the nameservers listed on your Cloudflare account (To find the NS values, go to your website's details page on Cloudflare, select DNS and scroll down to "Cloudflare Nameservers" heading. They will be listed here).
7. Update the nameservers on the Nameservers tab (next to "DNS") with your Cloudflare NS values.
6. That's it!

_It may take up to 24 hours for your SSL certificate to be generated._
Mine took only about an hour... and then, Voila!

As I mentioned above, the process was super easy.
The only
{% highlight ruby %}
  Barrier To Entry++
{% endhighlight %}
was figuring out where to change the NS settings on mydomain.com (the UI is not very intuitive). I needed to change both the nameservers in two places. It took me a few tries of tinkering with the setup to get this working.

**More background information on SSL and security if you're interested:**

[HTTPS - Wikipedia](https://en.wikipedia.org/wiki/HTTPS)

[Why HTTPS - Google Developers](https://developers.google.com/web/fundamentals/security/encrypt-in-transit/why-https)


**Food for thought:**
- Is an SSL certificate enough? It was easy to get the certificate so what's to stop scammers from doing the same, making visitors feel secure on fraudulent sites by displaying that little green lock as the while stealing CC numbers or personal information?
- What are security best practices for a more robust application (say a full stack app, db, hashed passwords, etc) as opposed to a simple frontend site?
- Unrelated... but I noticed my site redirects www.jenniferwiner.com to jenniferwiner.com. It drops the www. Why is this? Will visitors to my site notice this? Will it cause any security concerns?
