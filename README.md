# domain-redirects
Simple repository for setting up Digital Ocean Static Apps for doing domain redirects. By default, your base application will redirect to https://example.com, but you can change this in your domain settings once you've deployed to digital ocean using the button below:

[![Deploy to DO](https://www.deploytodo.com/do-btn-blue.svg)](https://cloud.digitalocean.com/apps/new?repo=https://github.com/SocksTheWolf/domain-redirects/tree/main&refcode=b6f00eb15df2)

You can click Skip to Review and then build the application. Everything is set up for you so you do not have to pay anything.

# Configuring Domains

This guide expects that you have already linked your domain to Digital Ocean [via this page](https://cloud.digitalocean.com/networking/domains). You can find a guide on how to do this properly [here]().

Once you have built and deployed the app for the first time (automatically done upon build), you will be taken to the settings screen. From here, you can edit your domains. Click on the Edit button highlighted in the box below.

[![Edit Domains](/images/domains-settings.png)]

Then click "+ Add Domain"

On this page, type in your domain name, confirm your hostname settings are correct in your domain registrar DNS.

[![Edit Domains](/images/www.png)]

**Note**: If you aren't using a cname based host like Google Sites, remember to also go back and add the `www.` version of your domain as well.

# Configuring Redirects
