:warning: In progress

---

# coreos-mgr

A CoreOS Cloud Init management webservice

## Usage

1. Visit https://coreos-mgr.not.implemented.com
1. Enter your S3 keys and bucket
1. Create a `cloud-config.yaml` template
1. Provide a host set in the form `myhost-{1..10}` or `myhost-a myhost-b`
1. Initialize machines with `coreos-cloudinit --from-url="https://s3.amazonaws.com/<bucket>/<hostname>"`

## Notes

* It's recommended that you set your machine's `HOSTNAME`, so you only need to replace `<hostname` with the shell replacement `${HOSTNAME}` in the command above.
* This is a pure client-side JavaScript application, there is only the GitHub file server, your keys are only sent to AWS. You can confirm this in your browser's developer tools.

## Todo

* etcd discovery service viewer

#### MIT License

Copyright © 2015 Jaime Pillora &lt;dev@jpillora.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.