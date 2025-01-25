# hidden-service

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/SimonHaas/hidden-service?quickstart=1)

Quickly host and access your very own `.onion` website.

``` shell
docker compose up -d

# Wait until: Bootstrapped 100%: Done
docker compose logs -f tor

# Get the address of your .onion site
docker compose exec tor onions

# You can see the keys of your site inside the tor container
docker compose exec tor ls -la /var/lib/tor/hidden_service
```

1. open your browser
2. set the SOCKS proxy to `localhost:9050`
3. browse to your own `.onion` website 🧅🚀

If you are using Github Codespaces in the browser you can use [webtop](https://github.com/SimonHaas/webspace) on port 3000 to open a remote instance of firefox.

Powered by [https://github.com/cmehay/docker-tor-hidden-service](https://github.com/cmehay/docker-tor-hidden-service)
