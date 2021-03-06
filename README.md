# TextScreen

Simple Twilio app for screening people before they text you. Make your Twilio number public-facing to get rid of (most) spammers.

## Setup

First, copy `config.example.yml` to `config.yml` and fill it in with the appropriate values.

### Storage

You can store conversation sessions either in-memory or in Redis. Check the config for instructions. Note that sessions stored in Redis will expire after 24 hours to prevent them from piling up. Sessions stored in-memory do not expire.

### Docker

There is a Docker image provided for easy setup:

#### Volumes

Place your config file at `/config.yml` in the container as a volume.

#### Ports

By default, the server listens on port `8080`, so bind that to something on your host. Or whatever. You can change this in the config.

## License

```
MIT License

Copyright (c) 2020 TJ Horner

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```