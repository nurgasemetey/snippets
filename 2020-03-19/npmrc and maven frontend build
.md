### npmrc and maven frontend build



[npm config set registry &lt;url&gt; impact other node installation · Issue #189 · eirslett/frontend-maven-plugin](https://github.com/eirslett/frontend-maven-plugin/issues/189 "npm config set registry &lt;url&gt; impact other node installation · Issue #189 · eirslett/frontend-maven-plugin")



[How should I set _auth in .npmrc when using a Nexus https npm registry proxy? - Stack Overflow](https://stackoverflow.com/questions/35043155/how-should-i-set-auth-in-npmrc-when-using-a-nexus-https-npm-registry-proxy "How should I set _auth in .npmrc when using a Nexus https npm registry proxy? - Stack Overflow")



[node.js - Setting up username and password for npm registry URL - Stack Overflow](https://stackoverflow.com/questions/50612549/setting-up-username-and-password-for-npm-registry-url "node.js - Setting up username and password for npm registry URL - Stack Overflow")


 

```shell
<execution>
						<id>npm install</id>
						<goals>
							<goal>npm</goal>
						</goals>
						<configuration>
							<arguments>install --registry=https://registry.npmjs.org/</arguments>
						</configuration>
						<phase>generate-resources</phase>
					</execution>

create npmrc file in working directory
_auth = <USERNAME>:<PASSWORD> (converted to base 64)
email = youremail@email.com
always-auth = true

$ echo -n 'username:password' | openssl base64

```
