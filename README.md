# Select the solution (net9.0 -or- net10.0)

Two versions of the same app are included in this repository.

* `net9.0` -> point-of-sale-9
* `net10.0` -> point-of-sale-10

Choose one of these according to the dotnet version installed on the machine.


## (optional) Install the required dotnet version

If `net9.0` and `net10.0` are not installed: install one of them according to the selected solution.

## (optional) Update the file `global.json` according to the dotnet version installed on you machine

Exapmple: `point-of-sale-9\src\global.json`

```json
{
  "sdk": {
    "version": "9.0.308",
    "workloadVersion": "9.0.308",
    "allowPrerelease": false,
    "rollForward": "disable"
  }
}
```


# Check workload list - Restore if required 

In the selected solution folder: 

```sh 
dotnet workload list
dotnet workload restore 
```


# Restore solution dependences 

In the selected solution folder: 

```sh
dotnet resrtore
```


# Run API Project 

In the selected solution, project `PointOfSale.API` folder:

```sh
dotnet build
dotnet run 
```


# Run App Project 

In the selected solution, project `PointOfSale.API` folder:

# Run on iPHone/iPhoneSimulator iOS:

```sh
dotnet build -t:Run -f net9.0-ios
```

# Run on MacOS:

```sh
dotnet build -t:Run -f net9.0-maccatalyst
```