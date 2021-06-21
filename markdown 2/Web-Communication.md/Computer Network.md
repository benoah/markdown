# What is a computer network?

> A network is a series of computers that are linked together in some way, either physically or electronically. The World Wide Web is dependent on computer networks and would literally cease to exist without these.

## DARPA/ARPANET – 1969

> Much of the computer technology that we take for granted today has its origins in military applications.

> The concept behind ARPANET was to enable robust communication between different computers.

## Vint Cerf, Bob Kahn & TCP/IP

> The idea of creating a standard for computer networking was the brainchild of two ARPA employees, Vint Cerf and Bob Kahn. They managed to address the two issues that had dogged networked computer communication and is still functional today.

> Circuit-switched networks are great for phone calls – most of the time, you are having a one-to-one conversation. But circuit switching, as we have seen, does not really work very well for computer networks.

# Transmission Control Protocol (TCP)

### What TCP does:

- Creates connections between networks
- Confirms delivery of each packet, or requests the packet be resent

# Internet Protocol (IP)

### What IP does:

- Confirms network identity
- Allows routing of information over networks
  -Ensures packets are delivered from source to destination

# IPv4 vs IPv6

> iP uses quad notation – 4 numbers, separated by periods. Each number is represented by 8 bits. So each number has a maximum value of 255. The total number of bits used for this version of the IP protocol is 32 bits. This quad notation is an example of IPv4 in action. We will come back to IPv4 later.

> If you do the math, you will see that this IP address format allows for over 4 billion unique addresses. While this was seen as more than enough in the 1980s, the internet is currently starting to reach a saturation point so a newer implementation of IP has been introduced - IPv6, which uses 128 bits. With 128 bits, up to 2128 unique addresses may be covered. Can we state this as a real world number? Of course, the IPv6 protocol can have:

# IPv4 vs IPv6

> Devices that are connected directly to the internet will have an IP address that is unique and cannot be reused anywhere else on the Internet. This is the difference between public and private IP addresses. A router with a public IP address can act as the "gateway" for a private network. Private IP addresses are reserved numbers which will only ever function as "private" and must go through a public gateway. As they are never publically used, they do not have to be unique and may be replicated for as many private networks as needed.

> If you want to send a document from your computer to your printer, you have no need to use the internet. Your router acts as the hub of your private network and "routes" your document to your printer. If you wanted to send that document to a friend in another country, it is likely you would have to do so by use of the public internet and your router would then act as a gateway to the internet at large.

# Subnet Mask

> A subnet mask segments an IP address into the network address and the host address. Subnetting can allow the network administrator to organize hosts into logical groups and this will increase both performance and the security of the network. The host address can be subnetted even further.

# Default Gateway

> The default gateway allows devices on one network to communicate with devices on another network. If there was no gateway, the network would be isolated from the outside. If your computer requests a website to load, that request first goes through your gateway before leaving your local network and reaching the internet.

# Static & Dynamic IP

**Static IPs allow you more control and are critical if the IP is going to be pointed at by things like hosting services, names servers, etc. Dynamic IPs are relatively hassle free; they are easy to set up and require little technical knowledge.**

_Static IPs are normally only important for public addresses where many devices or websites/servers refer to the IP (name servers are a good example of this). Other examples would be VPNs that hold a "whitelist" of "trustworthy" IPs. For these reasons, it is more common for businesses and specific services like hosting and email, to have static IPs._

_Dynamic IPs are more suitable for "private" addresses: IPs that are behind a router or web service. Dynamic Host Control Protocol (DHCP) makes it very easy to connect your device to a given network without having to specify an IP yourself as the router will automatically assign your device a dynamic IP._

# Network Ports

> An IP address can have a number of different services associated with it. You most likely work on your computer with multiple network operations happening at the same time - ever check your social media while waiting to get your email? This is where ports come into play. Each protocol (email, file transfer, and so on) has a commonly dedicated port. You can think of ports just like ports in a harbor – different network ports are for different protocols, just as different ports in a harbor are for different boats. Also, the address (both the destination and the source) remains the same. Ultimately, your data will get to your machine via one port or another.\*\*

> So how do modern networks keep from mixing all the data up? Different network tasks are assigned to different ports. There are 65,536 (216) possible ports. The first 1,024 (0-1,023) are well-known ports, used for established services such as email and ftp. HTTP, or HyperText Transfer Protocol, uses port 80, while HTTPS uses port 443. Ports 1,024-49,151 are registered ports, used for more specific services. They are granted by Internet Assigned Numbers Authority (IANA). You can have a look at the IANA's list of registered ports here.

You will see that some ports use UDP (User Datagram Protocol) transfer protocol instead of TCP. This is a somewhat more forgiving network transfer protocol and is most often used for "noncritical" transmission - such as audio/video streaming – where TCP "handshaking" is less important. With UDP, there is no acknowledgement of data receipt.\_

# Top Level Domains

\_When we talk about web domains, we are talking about addresses which are connected to servers or other devices. Top level domains, as the name implies, are the highest web domains in the domain name system hierarchy. There are currently over 1000 top-level domains and examples of them are .com, .org, and .net.

\_IP addresses are great, but a single 12-digit number is not easy to remember – imagine how difficult it would be to remember all the IP addresses of the websites you visit on a daily basis! This is where a Domain Name System (DNS) comes into play.

\_A DNS server will take an IP address and look it up in a table where it will find the domain name associated with the IP address. It will then send this name associated with this IP address and this is why you can type in words into your web browser, rather than just numbers. As long as a DNS server can find a name that matches the IP number, it will work. This also works in reverse – a DNS can translate a domain name to an IP address and this process is referred to as resolving.

\_While a "master list" is kept by DNS authority, it would be too much work for a single server to handle every single domain name request. For this reason, there are multiple domain name servers distributed around the globe. Each top-level domain has its own authoritative name server. If your local DNS does not have a name for a given IP address, it will contact other DNS servers to obtain it from them. DNS is also used for email addresses, instant messaging, and other instances where a name is easier to remember than an IP address.

## In summary, here is what the Domain Name System offers:

- Mapping of IP addresses to domain names and vice versa
- All mapping is stored in a database
- The DNS database is distributed

# Domain Name System Security Extensions (DNSSEC)

**DNSSEC is an attempt to prevent spoofing or DNS cache poisoning (fooling DNS servers into incorrectly resolving name/number pairs). This system does little to make DNS data private; rather, it focuses on authenticating existing DNS entities.**

## DNS Name Resolution Process

#### 1. Query the Recursive Resolver

- When you type a domain name (for example www.wikipedia.org) into your browser and hit enter, your browser sends a query over the Internet to a recursive DNS resolver.

#### 2. Find the Name Server’s IP

- The DNS Resolver then asks the Root Server "what is the IP address for the Name Server for the domain – www.wikipedia.org?" Root Servers run around the world and know the DNS info about top level domains like .com. The Top Level Domain server is able to answer with the address for the Name Server. This is still not the domain's IP address, but just the server that houses that domain.

#### 3. Ask the Name Server for the Domain’s IP

- The domain's Name Server is then asked by the Recursive Resolver what the webpage's IP address is.

#### 4. Display the Page

- The IP address is then sent back to the browser and it is then able to request the data from that IP address to display on your browser.

> Domain hierarchy
> .com (top level, managed by ICANN)
> apple.com (second level, managed by Verisign)
> www.apple.com (third level, managed by Apple)

## Pre-Web Networks

> Before the World Wide Web, a number of commercial computer-based user networks existed, like Compuserve and AOL. They worked on TCP/IP networks but they did not use Hypertext or have graphical user interfaces. Most networks were set up for text-based functions like chat, email, and file transfer. The standard speed for internet transmission was very slow; downloading a single file could take several minutes, or even longer. While these services offered some of the functionality of the Internet, they tended to be cumbersome to use, especially in the realm of user-friendliness.

> There were also services like Teletext and France's Minitel but these were even more limited. These were generally more passive services and would simply allow users to view various pages of information with a minimum of interactivity.

> As early as 1969, Douglas Engelbart gave a demonstration which included a number of elements of a computer system that were revolutionary. The name of the system being demonstarted was the oN-Line System, or NLS, and included the use of a computer mouse, Hypertext, associative linking, and the use of the window metaphor - all in a self-contained system. This demonstration influenced further work and related technologies at Xerox PARC (Palo Alto Research Center) as well as at companies like Apple Computer.

# HTML: The Birth of The World Wide Web

> While HTML is something most of us probably take for granted now, it was not so long ago that it was a radical idea. HTML is based on Hypertext which “goes beyond” ordinary text. The concept behind Hypertext is to create meaning through association, and here we will explore what that means.

## The library metaphor

> Imagine you go to your local library. You are looking for a book on a particular subject. You find this book, borrow it, and take it home. As you begin to read this book, you notice that another book is mentioned a number of times in the text. Eventually you realize that this book has some information you need, so you decide to go back to the library.

> You take out this second book, take it home, and repeat the process. Once again, you see this book mentions still other books, meaning more trips to the library. Instead of going to your local library every time you come across a footnote to a referenced text, wouldn’t it be great if these texts could be connected together in some logical way?

> The idea of establishing a connection between two texts is called an associative link. Associative links allow for nonlinear text access – which means that you may digress and explore other texts that are linked to the original instead of reading a book from cover to cover.

# HTML: The Birth of The World Wide Web cont.

### Tim Berners-Lee and the World Wide Web

> Tim Berners-Lee, an English computer scientist, worked at the largest internet node in Europe, CERN. During his time there, a lot of information was being shared but the process was cumbersome and time-consuming. Berners-Lee’s "great idea" was to combine the existing technologies of the Internet and Hypertext to create the World Wide Web. He wanted to be able to share knowledge and information in a "Web" of documents using Hypertext. Working with Robert Cailliau, he proposed a model for the World Wide Web and also developed the first web browser/editor, appropriately named WorldWideWeb.

> Berners-Lee chose not to license or patent the technology but allow it to be used by anyone. Some of the first web pages were descriptions of the technology and instructions on how it could be used. The world's first web server was based at CERN and the first web page was launched on the 6th of August, 1991. This page is still active, have a look.

> NCSA Mosaic was one of the first commercially available web browsers and is largely credited for popularizing the World Wide Web. It was easy to install and use, and supported a number of protocols (HTTP, FTP, NNTP, among others). Microsoft eventually licensed Mosaic as a basis for Internet Explorer in 1995.

# HyperText Transfer Protocol (HTTP)

> Berners-Lee chose not to license or patent the technology but allow it to be used by anyone. Some of the first web pages were descriptions of the technology and instructions on how it could be used. The world's first web server was based at CERN and the first web page was launched on the 6th of August, 1991. This page is still active, have a look.

**NCSA Mosaic was one of the first commercially available web browsers and is largely credited for popularizing the World Wide Web. It was easy to install and use, and supported a number of protocols (HTTP, FTP, NNTP, among others). Microsoft eventually licensed Mosaic as a basis for Internet Explorer in 1995.
HyperText Transfer Protocol (HTTP)
The network protocol used to distribute and link web pages, also developed by Berners-Lee's team, is called HyperText Transfer Protocol and it ensures that transfer functions according to a specific set of rules. It essentially functions as a client/server protocol where the client (a web browser) will request information from a server (a web server).**

> Like many other modern network protocols, the HTTP protocol is specifically designed to function within the framework of the TCP/IP protocol. Different protocols are designed for certain kinds of functionality; File Transfer Protocol (FTP), for example, is specifically designed for the transfer of files. HTTP protocol is specifically designed for the transfer of HTML documents.

You may have noticed the "http" at the start of many web addresses. These 4 letters are important as they determine the kind of communication your browser will be having with the server. Many modern browsers will do the work for you and enter HTTP when you go to a specific web page.

> A standard HTTP session will consist of a query from the client to the server; once the initial query is confirmed, the transfer of information may begin. If the query is not confirmed because the web address is incorrect or there is a connection problem, no data transfer will occur. A "success" HTTP response is 200; if the resource cannot be found, the response will be 404. There are a number of HTTP responses, a more complete list is available here.

This simple query-response is the basis for all HTTP communication and more advanced forms of query response are also supported, such as authentication, where request may be answered with the demand of a username and password. There are also instances where a query may include various methods; a good example of this would be a database search with an included keyword. In this case, the query method may be more complex.

> The two earliest and most widely used HTTP query forms are GET and POST. GET is simply a method to retrieve data from a given server. Here is an example of a GET query:

> http:www.cats.org/survey/form.php?name1=value1

> You will notice this looks slightly different from a bare-bones web address, as there is some extra information in the query from the question mark onwards. The ? states that certain values will be submitted along with the query and the name/value pair are parameters that may be sent to make the query more specific.

**The GET query is considered "safe" as no critical information is sent to the server. There may be instances where GET is inadequate, however; such as when submitting personal information from a web form to a database. In this case, the POST query may be used. The POST query has no limit on length, but will never be stored as a bookmark or browser history as a GET query may be. The POST data will also never be shown in the URL.
URIs, URLs, & URNs**

> Identifying an HTTP resource has to be performed in a specific way; when we think of a "web address", in the broadest sense we are actually referring to a Uniform Resource Identifier (URI). A URI is a string of text that identifies a given resource ("resource" being a page, image, or other item that is available).

\_A Uniform Resource Name (URN) refers to a given name of a resource within a given domain. It will not specify the specific location of the resource. You may think of a URN as a person's name; you know the name of the person, but you are not given their address. A Uniform Resource Locator (URL) is the term that you are most likely familiar with. This gives the specific location of a resource For this reason, a URL is sometimes referred to as a web address.
HTML as a language

// HTML is a markup language. A markup language is primarily designed for processing, defining, and presenting text. Because HTML is text-based, HTML files are essentially text files but it does also support many different media types including images, video and audio.

> HTML was originally based on standards set out by SGML (Standard Generalized Markup Language) which is an established standard for document setup. HTML5, the latest version of HTML, is no longer based on SGML.

> HTML is not the only existing markup language – there are dozens of different markup languages, each developed for a specific task. Another example of a widely used markup language is Extensible Markup Language, or XML which has also played a role in HTML development.
