# goshimmer-webauth

**JWT authentication for IOTA Shimmer prototype**

 Use with **[goshimmer-ui](https://github.com/Evanfeenstra/goshimmer-ui)** to secure access to your Shimmer node via username/password combination and JWT. 

Usage:
```
git clone https://github.com/Evanfeenstra/goshimmer-webauth.git plugins/webauth
```

then in **main.go**, import the package:
```
"github.com/iotaledger/goshimmer/plugins/webauth"
```

and add the plugin to main()
```
webauth.PLUGIN,
```

build
```
go build -o shimmer
```

add these three environment variables:
```
export JWT_KEY=*****
export UI_USER=*****
export UI_PASS=*****
```

and run
```
./shimmer --node-enable-plugins "webauth ui spammer"
```

### navigate to **[localhost:8080/ui](http://localhost:8080/ui)** in your browser!

Then enter your **UI_USER** and **UI_PASS** into the Username and Password fields to access your node! This plugin secures *all* the **webapi** routes, so you can open port 8080 and securely configure your node from anywhere.

