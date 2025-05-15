# Symxify

Symxify is the foundation for all of our products at Symxify. It's how we build and maintain bespoke tools, as well as build our first-party, fully-featured products like the [Member Relationship Manager](../mrm/).

### What is Symxify?

Symxify is a wrapper around SymXchange. Think of it as a gateway into your gateway.

![alt text](/assets/image.png)

There are two versions of Symxify - a fully self-hostable, open-source version that's completely free to download and run. All you need to do is configure it with your Sym's connection properties and you'll be off to the races.

There's also [Managed Symxify](https://memberwise.io/products/symxify), our managed solution for Symxify. Manage Symxify allows you to manage multiple connections for development and production, among other awesome quality of life enhancements to the SymXchange experience. 

Symxify allows you to quickly build integrations with your Symitar core by providing you language-agnostic infrastructure and tools.



### Why is this needed?

In the year 2025 (when this documentation was written), SOAP has been a "deprecated" for almost 15 years.

![alt text](/assets/image2.png) 

Jack Henry decided to use SOAP to implement it's fully-featured API rather than REST. SOAP is notoriously difficult to work with in modern programming languages. Symxify takes the burden of needing to construct fully-qualified SOAP requests and abstracts it away from you completed. All you, as a developer, need to do is write your code the way you would against a normal API - RESTfully.

