## Definition
OS-only Runtimes is when there is not preinstalled programming language and language specific libraries installed when you want to compile your language or programs to be used.

What this essentially is the operating system environment without a preinstalled programming language runtime 

There are 3 cases when to use OS-only-runtimes:
1. Native ahead-of-time (AOT) compilation
Languages such as Go, Rust, and C++, .NET Native AOT, Java GraaIVM Native complie natively to an executable binary, which doesn't require a dedicated laguage runtime. 

You must include a runtime interface client in your binary
You must compile your binary for a Linu environment for the same instruction set architecture

2. Third-party runtimes
Runtimes such as Bref for PHP
Swift AWS Lambda Runtime for Swift

3. Custom runtimes
Build your own runtime for a language or language version that Lambda doesn't provide a managed runtime 

The OS-only runtimes:
- Amazon Linux 2 
- Amazon Linux 2023