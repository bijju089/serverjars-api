# Minecraft Server Jars (API)

ServerJars API endpoint (Free to use)
### URL
**MAIN**: <br>
`https://api.serverjars.in`
## Endpoint
### 1. Fetch All Jar Types
Retrieve a list of all available jar types. <br>
**Endpoint:** <br>
**GET** `/v1/serverjars/fetchTypes`
```json
{
  "response": {
    "modded": ["mohist", "fabric", "forge"],
    "proxies": ["waterfall", "bungeecord", "velocity"],
    "vanilla": ["vanilla", "snapshot"],
    "servers": ["paper", "purpur", "sponge"]
  }
}
```
### 2. Fetch All Versions for a Category
Retrieve all versions available for a specific category. <br>
**Endpoint:** <br>
**GET** `GET /v1/serverjars/fetchAll/{category}` <br>
Parameters: The `{category}` of server jars (e.g., paper, fabric, forge). <br>
  **Example Request**: <br>
     **GET** `GET /v1/serverjars/fetchAll/paper`
```json
{
  "response": [
    {
      "version": "1.21.1",
      "file": "paper-1.21.1.jar"
    }
  ]
}
```
### 3. Fetch a Specific Jar
Retrieve the download URL for a specific jar file based on its type and version. <br>
**GET** `/v1/serverjars/fetchJar/{category}/{minecraftversion}`
```json
{
  "response": {
    "url": "https://cdn.cxstudios.in/uploads/serverjars/jars/paper-1.21.jar"
  }
}
```

