# Blazor Wasm + Serverless Template
This is a playground for modifying the Blazor WebAssembly project templates to enable an option to have Blazor Wasm + Serverless (via Azure Functions) as an option.  It is experimental and additive to the base Wasm templates provided in the SDK.

## How to use
From a terminal prompt:

`dotnet new blazorwasm --serverless`

This will create a solution with three projects:

* Client - the Blazor Wasm client app which will reference the shared components
* Serverless - An Azure Functions project with one HttpTrigger function and also references the shared components
* Shared - shared components in a .NET Standard lib

This is very similar to the `dotnet new blazorwasm --hosted` option but swaps out the Server project for a Serverless one.

## Warning - Experimental
This is just an experimental playground.  Lots not figured out here like:

* getting the base URI for the functions into a config easily
* options for exposing functions options (storage + authentication mode)
* multi-startup solution to F5 immediately