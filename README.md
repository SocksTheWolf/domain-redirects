# domain-redirects
Simple repository for setting up DigitalOcean Static Apps for doing domain redirects. By default, your base application will redirect to https://example.com, but you can change this in your domain settings once you've deployed to DigitalOcean using the button below:

[![Deploy to DO](https://www.deploytodo.com/do-btn-blue.svg)](https://cloud.digitalocean.com/apps/new?repo=https://github.com/SocksTheWolf/domain-redirects/tree/main&refcode=b6f00eb15df2)

(Small Disclosure Note: I inject my refcode into the project setup URL, so if you ever buy anything on DigitalOcean, I get a small cut, but this entire project is free for up to 3 uses, so I'll probably not make anything)

You can click Skip to Review and then build the application. Everything is set up for you so you do not have to pay anything.

# Configuring Domains

This guide expects that you have already linked your domain to Digital Ocean [via this page](https://cloud.digitalocean.com/networking/domains). You can find a guide on how to do this properly [here](https://docs.digitalocean.com/products/networking/dns/how-to/add-domains/).

Once you have built and deployed the app for the first time (automatically done upon build), you will be taken to the settings screen. From here, you can edit your domains. Click on the Edit button highlighted in the box below.

![Edit Domains](/images/domains-setting.png)

Then click "+ Add Domain"

On this page, type in your domain name, confirm your hostname settings are correct in your domain registrar DNS.

![Domains Settings](/images/www.png)

**NOTE**: If you aren't using a CNAME based host like Google Sites, remember to also go back and add the `www.` version of your domain as well.

# Configuring Redirects

Once your domains are properly set up, you are now ready to set up the routing rules.

Click the "HTTP Routes Redirect" edit button on your settings page to get started.

![HTTP Routes Redirect Direction](/images/http-routes.png)

Once clicked, a new window will appear for setting routing rules.

![HTTP Routing Rules](/images/routerules.png)

1. Route Path: This is the location on your domain that triggers the routing. A single slash will mean going to the website by with no pathing will trigger the redirection.
2. Redirect URI: This will be where on the Redirect Authority you should navigate to. If you leave it empty, it will use the value from the value in the first step. If you were redirecting to twitch, you should put a `/CHANNELNAME` in this field
3. Redirect Authority: The domain that you would be redirecting to. If you were redirecting to Twitch, this would be a simple `twitch.tv`
4. If you wanted to add more redirects, say something like `yourdomain.tld/store` you could do so by adding more routes.

Any future additions _should always_ have the redirection scheme set to `https`.

**NOTE**: REMEMBER TO SAVE AFTER CONFIGURING. Your project may take a bit of time to build once you have done this.

# Conclusion

From here on out, you are done. This will make your URL redirects always work, even if you use a registrar such as namecheap without having to pay for webhosting to handle the redirects. The default DigitalOcean plan allows you to make three of these apps for free for an account. 

Enjoy the good life of having a simple redirection URL for your socials.

You can find me on https://wolf.stream or https://wolf.stream/bsky (wolf.stream's redirects uses this project)
