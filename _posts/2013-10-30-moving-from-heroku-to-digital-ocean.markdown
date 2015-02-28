---
layout:     post
title:      "Moving from Heroku to Digital Ocean"
subtitle:   "how I reduced my hosting bill with 80% with better performance"
date:       2013-10-30 12:00:00
author:     "Martin Kretz"
header-img: "img/post-bg-01.jpg"
---

{<1>}![DigitalOcean logo](/content/images/2013/Oct/digital_ocean_logo_1200x900.png)

## Why Heroku?
[Heroku](http://heroku.com) is fantastic. I've been using it for years. It's reliable and hides all the stuff  that you don't want to worry about as an app developer (failover, load balancing, process monitoring, backups, security patches, etc, etc).

## Why NOT Heroku?
Heroku can be expensive.

To run a Rails app with 1 GB RAM ($34), a database ($9), a worker thread ($34) and SSL support ($20) will cost **$97 per month on Heroku**.

If you have a profitable app with many paying customers that is probably ok. I'd say it is worth $97 per month not having to worry about servers and instead focus on your what's more important - your apps, customers and business.

But what if your app is not making any money yet? And what if you have many apps like this?

If you know your way around a server, and have some time to configure and maintain it, you can save some money by doing it yourself.

## Why DigitalOcean?
[DigitalOcean](https://www.digitalocean.com/?refcode=138e6c803d00) is a relatively new cloud server provider (started 2012) and it has been getting a lot of attention due to its all SSD storage and low priced servers starting at $5 per month.

To run a Rails app like the example above, 2GB RAM should be enough. That will be **$20 per month on DigitalOcean**.

To compare, 2 GB of RAM would cost $40 per month on [Linode](https://www.linode.com/?r=f818067ccf38443121c95f2554c6031c51659031), and $44 per month on [Amazon EC2](http://aws.amazon.com/ec2/pricing/#on-demand).

Please note that I am not taking storage, bandwith, transfer costs or support level into account here. If you have special needs this needs to be factored in.

## Performance comparison
I compared load times from the **app with same source code** running on Heroku and DigitalOcean. I did 30 requests to each service to get the load time of a page. The page did a few database queries per load.

Surprisingly, **DigitalOcean has 40-50% faster load times**.

#### Heroku
  Min: 		0.538s
  Max: 		1.175s
  Average:	0.811s

#### DigitalOcean
  Min: 		0.248s
  Max: 		0.798s
  Average:	0.502s

## Conclusion
If you:

* Have an app without enough paying users
* Have the time to set up a Linux server
* Think fiddling with servers is **awesome**!

Then YES, a move to [DigitalOcean](https://www.digitalocean.com/?refcode=138e6c803d00) can save you money today! If you use [this link](https://www.digitalocean.com/?refcode=138e6c803d00) you get a $10 credit!


---

If you like this you should [follow me on Twitter](https://twitter.com/martinkretz).

_Note: I included affiliate links to DigitalOcean and Linode. It does not affect my opinions or recommendations of those services. Use the links if you want to support future blog posts like this._
