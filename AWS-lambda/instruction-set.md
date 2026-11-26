## Definition
There are two available instruction architectures available for Lambda or in other words, there are two CPU architectures that AWS Lambda supports: 
- arm64: 64 bit ARM architecture, for the AWS Graviton2 processor
- x86_64: 64 bit architecture, for x86-based processors 

An Instruction set are a set of opscode that represent operations the CPU can perform

Arm64 has a smaller instruction set therefore programs built against arm are more efficient and as a result are more cost effective. 

For a program to run a specific architecture the language has to turn into a machine language such (assembly code) which in turn is calling opcodes