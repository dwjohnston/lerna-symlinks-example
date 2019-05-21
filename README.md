# Instructions

System info: 

I'm using VSCode 1.34.

0. Run `lerna bootstrap`. 

1. Open two terminals, one to `packages/package-a` one to `packages/package-b`. 

2. Run `npm start` in each of these. 

3. Open `packages/package-a/src/package-a.ts` in VSCode. 

4. Observe that you have a type error 

  > Property 'b' is missing in type '{ a: string; }' but required in type 'Foo'.ts(2741)

5. In `packages/package-b/src/package-b.ts` change the b property to optional. (Add a `?` to it). 

6. Observe that the package has recompiled. See in the lib folder the d.ts file has updated. 

7. Observe that in `package-a.ts` the error is still showing. **This is what I want to solve**. 

8. You can get rid of the error by ctrl+clicking into the `Foo` interface declaration, then going back to the `package-a.ts` file. But this is a pain. 

