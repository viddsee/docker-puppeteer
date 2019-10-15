### What is this?
A Dockerfile image built referencing [GoogleChrome Puppeteer guide](https://github.com/GoogleChrome/puppeteer/blob/93843592da58efcb28cf740dd7dbfa9f04061fc8/docs/troubleshooting.md#running-on-alpine)

It is versioned with Puppeteer version (Latest: 1.17.0)

### How to use?
> Use at your own risk

```js
this.getBrowserPromise = puppeteer.launch({
  executablePath: '/usr/bin/chromium-browser',
  args: [
    '--no-sandbox',
    '--disable-setuid-sandbox',
  ],
});
```

### Development

#### Publishing
```sh
docker build -t amoshydra/puppeteer:1.17.0-dubnium .

docker tag amoshydra/puppeteer:1.17.0-dubnium amoshydra/puppeteer:1.17.0-dubnium
docker push amoshydra/puppeteer:1.17.0-dubnium

docker tag amoshydra/puppeteer:1.17.0-dubnium amoshydra/puppeteer:latest
docker push amoshydra/puppeteer:latest
```
