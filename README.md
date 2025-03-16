# iOS Firebase Test
> An iOS native app for testing a firebase backend. Sort of like Postman.

### Why Not Postman?
You may ask why not just use Postman. There are multiple reasons why it makes more sense to develop my own app for this. My first thought was, since I'm supporting an iOS app, I should have a better understanding of how the Firebase SDK for Swift is being used. I wanted to know more about Firebase authentication flow in particular.

### Digging into the App
The app I am supporting is already built and has a substantial amount of functionality in use. Part of understanding the logs and metrics being recorded by the Firebase backend is gaining a better understanding from the user device what is going on. I started to dig into the Swift codebase and it's massive. Since I have very little native app development experience, it was overwhelming. At that point I realized that just understanding the auth flow comprehensively would be extremely powerful and useful.

### Auth Issues at Scale
Most issues that I encounter at scale and in enterprise trace back to authentication, authorization, trust certificates, etc. In short, most issues are related to identity management once you factor in severity. That said, auth is typically not something that is heavily customized. You may design fine grained permission roles, but you're almost certainly not going to hack on the auth flow structure nor are you going to attempt to modify the protocols and practices of authentication and authorization or encryption.

### Permissions and IaC
Another category of issue was navigating carefully-governed permission boundaries that I put in place for an organization that I'm working for their security. By managing infrastructure with IaC, I can rapidly develop improvements in a sandbox in my own organization where I have elevated privileges. This way I can request specific fine-grained least privilege grants for exactly what capabilities I need in the form of code.

### Trust Certificate Concerns
I became concerned that trying to hook the existing Swift codebase up to my organization's Firebase backend would cause issues with the trust certificates. While we do ultimately plan to set up an end-to-end development environment for the Swift team, I'm not entirely sure what that whole process looks like. I come from a web background and a lot of this is new to me. Creating my own basic iOS app was a way to be able to quickly set up an end-to-end system so that I can identify all of the permissions, certificates, and infrastructure that I need so that I can build a pipeline with my own organization and then know precisely what I need to ask of whom and effectively lead this team from a DevOps and infrastructure management perspective.

### LLM Tools and Next Steps
Finally, some of the LLM-based development tools like Claude and Grok have made such an undertaking relatively quick and easy, especially since I will be working with basic stuff and not really breaking new ground. I also plan to add in more and more of the other standard functionality of the existing Swift codebase after I master auth. My expectation is that once I get to the novel IP, I will be able to coordinate with the Swift team and the organization owner and pivot to setting up the development environment within their organization.

### Future Goals
Hopefully by then I will understand enough about Swift development to work more closely with them with regards to the Firebase interface. I would like to be able to do effective code reviews on pull requests. As this system scales, I will need to analyze various logs and metrics and at times tie performance, cost, and security issues back to potential problems in the Swift code. I also want to have a hand in automated test coverage development.

### Long-Term Value
Looking forward, there is additional value. This puts me in a better position to help with development of an Android app. There is also the concern of outgrowing Firebase. Eventually, it will not be cost effective to rely entirely on Firebase for a backend. When we need to migrate to a more mature API with self-managed infrastructure, it will help me plan for the transition better if I have a deep technical understanding of how these apps interface with the Firebase backend.
