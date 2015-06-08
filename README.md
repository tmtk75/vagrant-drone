# README

# Getting Started
Referred <http://readme.drone.io/setup/config/github/>

- Rename `drone.toml.sample` to `drone.toml`, which will be copied to `/etc/drone` in the VM during provisining phase.
- Take a pair of Client ID/Secret from <https://github.com/settings/developers>.
- Fill following fields of `drone.toml` with them.
```
[github]
client="xxxxxxxxxxxxxxxxxxxx"
secret="40ed8bf91e8bc68e0716067aa1a47293a1691074"
#orgs=[]
open=true
```
- Bring up the VM, `vagrant up`
- Open `http://localhost:8080` with your browser.
