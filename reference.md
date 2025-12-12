# Reference

## McpServer

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">callTools</a>({ ...params }) -> Klavis.CallToolResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Calls a tool on a specific remote MCP server, used for function calling. Eliminates the need for manual MCP code implementation.
Under the hood, Klavis will instantiates an MCP client and establishes a connection with the remote MCP server to call the tool.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.callTools({
    serverUrl: "serverUrl",
    toolName: "toolName",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.CallToolRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">listTools</a>({ ...params }) -> Klavis.ListToolsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists all tools available for a specific remote MCP server in various AI model formats.

This eliminates the need for manual MCP code implementation and format conversion.
Under the hood, Klavis instantiates an MCP client and establishes a connection
with the remote MCP server to retrieve available tools.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.listTools({
    serverUrl: "serverUrl",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.ListToolsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">createStrataServer</a>({ ...params }) -> Klavis.StrataCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Strata MCP server.

Parameters:

- servers: Can be 'ALL' to add all available Klavis integration, a list of specific server names, or null to add no servers
- externalServers: Optional list of external MCP servers to validate and add
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.createStrataServer({
    userId: "userId",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.StrataCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">addServersToStrata</a>({ ...params }) -> Klavis.StrataAddServersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add servers to an existing Strata MCP server.

Note: After adding servers, you need to reconnect the MCP server so that list_tool can be updated with the new servers.

Parameters:

- servers: Can be 'ALL' to add all available servers, a list of specific server names, or null to add no servers
- externalServers: Optional list of external MCP servers to validate and add
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.addServersToStrata({
    strataId: "strataId",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.StrataAddServersRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">deleteServersFromStrata</a>(strataId, { ...params }) -> Klavis.StrataDeleteServersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete servers from an existing Strata MCP server.

Note: After deleting servers, you need to reconnect the MCP server so that list_tool can be updated to reflect the removed servers.

Parameters:

- strataId: The strata server ID (path parameter)
- servers: Can be 'ALL' to delete all available Klavis integration, a list of specific server names, or null to delete no servers
- externalServers: Query parameter - comma-separated list of external server names to delete

Returns separate lists for deleted Klavis servers and deleted external servers.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.deleteServersFromStrata("strataId", {
    externalServers: "externalServers",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**strataId:** `string`

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.DeleteServersFromStrataMcpServerStrataStrataIdServersDeleteRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getStrataServer</a>(strataId) -> Klavis.StrataGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get information about an existing Strata MCP server instance.

Returns the strata URL, connected klavis servers, connected external servers (with URLs),
and authentication URLs for klavis servers.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.getStrataServer("strataId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**strataId:** `string`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">listStrataRawActions</a>(strataId, { ...params }) -> Klavis.StrataRawActionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Fetch raw actions (all underlying actions) for a specific integration within a Strata MCP instance.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.listStrataRawActions("strataId", {
    server: "Affinity",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**strataId:** `string` — The strata server ID

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.ListStrataRawActionsMcpServerStrataStrataIdRawActionsGetRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getStrataAuth</a>(strataId, serverName) -> Klavis.StrataGetAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves authentication data for a specific integration within a Strata MCP server.

Returns the authentication data if available, along with authentication status.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.getStrataAuth("strataId", "Affinity");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**strataId:** `string` — The strata server ID

</dd>
</dl>

<dl>
<dd>

**serverName:** `Klavis.McpServerName` — The name of the Klavis MCP server to get authentication for (e.g., 'GitHub', 'Jira')

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">deleteStrataAuth</a>(strataId, serverName) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes authentication data for a specific integration within a Strata MCP server.

This will clear the stored authentication credentials, effectively unauthenticating the server.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.deleteStrataAuth("strataId", "Affinity");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**strataId:** `string` — The strata server ID

</dd>
</dl>

<dl>
<dd>

**serverName:** `Klavis.McpServerName` — The name of the Klavis MCP server to delete authentication for (e.g., 'github', 'jira')

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">setStrataAuth</a>({ ...params }) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sets authentication data for a specific integration within a Strata MCP server.

Accepts either API key authentication or general authentication data.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.setStrataAuth({
    strataId: "strataId",
    serverName: "Affinity",
    authData: {},
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.StrataSetAuthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">createServerInstance</a>({ ...params }) -> Klavis.CreateServerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a URL for a specified MCP server,
validating the request with an API key and user details.
Returns the existing server URL if it already exists for the user.
If OAuth is configured for the server, also returns the base OAuth authorization URL.
Note that some servers have hundreds of tools and therefore only expose the Strata tools.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.createServerInstance({
    serverName: "Affinity",
    userId: "userId",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.CreateServerRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">createSelfHostedServerInstance</a>({ ...params }) -> Klavis.CreateSelfHostedServerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates an instance id for a self-hosted MCP server,
validating the request with an API key and user details.
The main purpose of this endpoint is to create an instance id for a self-hosted MCP server.
The instance id is used to identify and store the auth metadata in the database.
Returns the existing instance id if it already exists for the user.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.createSelfHostedServerInstance({
    serverName: "Affinity",
    userId: "userId",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.CreateSelfHostedServerRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getServerInstance</a>(instanceId) -> Klavis.GetInstanceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Checks the details of a specific server connection instance using its unique ID and API key,
returning server details like authentication status and associated server/platform info.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.getServerInstance("instanceId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**instanceId:** `string` — The ID of the connection integration instance whose status is being checked. This is returned by the Create API.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">deleteServerInstance</a>(instanceId) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Completely removes a server connection instance using its unique ID,
deleting all associated data from the system.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.deleteServerInstance("instanceId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**instanceId:** `string` — The ID of the connection instance to delete.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getInstanceAuthData</a>(instanceId) -> Klavis.GetAuthDataResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves the auth data for a specific integration instance that the API key owner controls.
Includes access token, refresh token, and other authentication data.

This endpoint includes proper ownership verification to ensure users can only access
authentication data for integration instances they own. It also handles token refresh if needed.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.getInstanceAuthData("instanceId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**instanceId:** `string` — The ID of the connection integration instance to get auth data for.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">deleteInstanceAuth</a>(instanceId) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes authentication data for a specific server connection instance.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.deleteInstanceAuth("instanceId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**instanceId:** `string` — The ID of the connection instance to delete auth for.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getTools</a>(serverName, { ...params }) -> Klavis.ListToolsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get tools information for any MCP server.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.getTools("Affinity", {
    format: "openai",
    legacy: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**serverName:** `Klavis.McpServerName` — The name of the target MCP server. Case-insensitive (e.g., 'google calendar', 'GOOGLE_CALENDAR', 'Google Calendar' are all valid).

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.McpServerGetToolsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getAllMcpServers</a>() -> Klavis.GetMcpServersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all MCP servers with their basic information including id, name, description, and tools.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.getAllMcpServers();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">setInstanceAuth</a>({ ...params }) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sets authentication data for a specific integration instance.
Accepts either API key authentication or general authentication data.
This updates the auth_metadata for the specified integration instance.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.setInstanceAuth({
    instanceId: "instanceId",
    authData: {},
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.SetAuthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">listRawActions</a>(instanceId) -> Klavis.RawActionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Fetch raw actions (all underlying actions) for a specific integration instance.

This endpoint takes an instance ID, and then fetches the raw actions with categories.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.listRawActions("instanceId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**instanceId:** `string` — The instance ID for the server connection

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getOauthUrl</a>() -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mcpServer.getOauthUrl();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `McpServer.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## WhiteLabeling

<details><summary><code>client.whiteLabeling.<a href="/src/api/resources/whiteLabeling/client/Client.ts">createWhiteLabeling</a>({ ...params }) -> Klavis.WhiteLabelingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Saves OAuth white labeling information, or updates existing information if the `client_id` matches.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whiteLabeling.createWhiteLabeling({
    client_id: "client_id",
    client_secret: "client_secret",
    server_name: "Airtable",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.CreateWhiteLabelingRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhiteLabeling.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.whiteLabeling.<a href="/src/api/resources/whiteLabeling/client/Client.ts">getWhiteLabelingByClientId</a>(clientId) -> Klavis.WhiteLabelingResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves white labeling information for a specific OAuth client ID.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whiteLabeling.getWhiteLabelingByClientId("client_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clientId:** `string`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhiteLabeling.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## User

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getUserIntegrations</a>(userId) -> Klavis.GetUserIntegrationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all available integrations (MCP server names) by user ID.
Returns a list of integration names and their authentication status.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getUserIntegrations("userId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userId:** `string` — The external user ID

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `User.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getUserByUserId</a>(userId) -> Klavis.GetUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get user information by user_id.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getUserByUserId("userId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userId:** `string` — The identifier for the user to fetch.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `User.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">deleteUserByUserId</a>(userId) -> Klavis.DeleteUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a user and all associated data by user_id.
Users cannot delete their own accounts.
This operation will permanently remove all user data.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.deleteUserByUserId("userId");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userId:** `string` — The identifier for the user to delete.

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `User.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getAllUsers</a>({ ...params }) -> Klavis.GetAllUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all users that have been created under your account, with support for pagination.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getAllUsers({
    page_size: 1,
    page_number: 1,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.GetAllUsersRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `User.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">setUserAuth</a>({ ...params }) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sets authentication data for a specific integration for a user.

Accepts either API key authentication or general authentication data.
This updates the auth_metadata for the specified user's integration instance.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.setUserAuth({
    userId: "userId",
    serverName: "Affinity",
    authData: {},
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.SetUserAuthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `User.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getUserAuth</a>(userId, serverName) -> Klavis.GetUserAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves authentication data for a specific integration for a user.

Returns the authentication data if available, along with authentication status.
Includes token refresh handling if needed.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getUserAuth("userId", "Affinity");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userId:** `string` — The identifier for the user

</dd>
</dl>

<dl>
<dd>

**serverName:** `Klavis.McpServerName` — The name of the MCP server (e.g., 'GitHub', 'Jira')

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `User.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">deleteUserAuth</a>(userId, serverName) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes authentication data for a specific integration for a user.

This will clear the stored authentication credentials, effectively unauthenticating the integration.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.deleteUserAuth("userId", "Affinity");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userId:** `string` — The unique identifier for the user

</dd>
</dl>

<dl>
<dd>

**serverName:** `Klavis.McpServerName` — The name of the MCP server to delete authentication for (e.g., 'github', 'jira')

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `User.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Oauth

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeSlack</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Slack OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- user_scope: Optional user-specific scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeSlack({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    user_scope: "user_scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeSlackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeGithub</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start GitHub OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeGithub({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeGithubRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeGitlab</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start GitLab OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeGitlab({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeGitlabRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeSupabase</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Supabase OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeSupabase({
    instance_id: "instance_id",
    client_id: "client_id",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeSupabaseRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeNotion</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Notion OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeNotion({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeNotionRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeJira</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Jira OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeJira({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeJiraRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeConfluence</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Confluence OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeConfluence({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeConfluenceRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeWordpress</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start WordPress OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeWordpress({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeWordpressRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeGmail</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Gmail OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeGmail({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeGmailRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeGdrive</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Google Drive OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeGdrive({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeGdriveRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeGcalendar</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Google Calendar OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeGcalendar({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeGcalendarRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeGsheets</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Google Sheets OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeGsheets({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeGsheetsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeGdocs</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Google Docs OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeGdocs({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeGdocsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeAttio</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Attio OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeAttio({
    instance_id: "instance_id",
    client_id: "client_id",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeAttioRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeSalesforce</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Salesforce OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
- instance_url: Optional Salesforce instance URL for sandbox or custom domains
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeSalesforce({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
    instance_url: "instance_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeSalesforceRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeAsana</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Asana OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeAsana({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeAsanaRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeLinear</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Linear OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeLinear({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeLinearRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeClose</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Close OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeClose({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeCloseRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeClickup</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start ClickUp OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeClickup({
    instance_id: "instance_id",
    client_id: "client_id",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeClickupRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeAirtable</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Airtable OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeAirtable({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeAirtableRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeHubspot</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start HubSpot OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeHubspot({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeHubspotRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeLinkedin</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start LinkedIn OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeLinkedin({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeLinkedinRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeCanva</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Canva OAuth flow with PKCE

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated, e.g., "design:meta:read profile:read")
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeCanva({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeCanvaRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeXero</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Xero OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeXero({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeXeroRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeDropbox</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Dropbox OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeDropbox({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeDropboxRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeBox</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Box OAuth 2.0 flow

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeBox({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeBoxRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeQuickbooks</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start QuickBooks OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- environment: QuickBooks environment to authorize ('sandbox' default)
- scope: Optional scopes to request (space-separated). Default is 'com.intuit.quickbooks.accounting'
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeQuickbooks({
    instance_id: "instance_id",
    client_id: "client_id",
    environment: "sandbox",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeQuickbooksRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeZendesk</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Zendesk OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
- subdomain: Zendesk subdomain for the account being connected
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeZendesk({
    instance_id: "instance_id",
    subdomain: "subdomain",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeZendeskRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeStripe</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Stripe Connect OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeStripe({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeStripeRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeCalcom</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Cal.com OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeCalcom({
    instance_id: "instance_id",
    client_id: "client_id",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeCalcomRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeVercel</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Vercel OAuth flow using integration pattern

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- client_slug: Vercel integration slug (required for integration-based OAuth)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeVercel({
    instance_id: "instance_id",
    client_id: "client_id",
    client_slug: "client_slug",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeVercelRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizePipedrive</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Pipedrive OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizePipedrive({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizePipedriveRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeFigma</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Figma OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeFigma({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeFigmaRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeKlaviyo</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeKlaviyo({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeKlaviyoRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizePagerduty</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start PagerDuty OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizePagerduty({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizePagerdutyRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeDocusign</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start DocuSign OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeDocusign({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeDocusignRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeDialpad</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Dialpad OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
- code_challenge: PKCE code challenge for enhanced security
- code_challenge_method: PKCE code challenge method
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeDialpad({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
    code_challenge: "code_challenge",
    code_challenge_method: "code_challenge_method",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeDialpadRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeOnedrive</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeOnedrive({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeOnedriveRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeOutlook</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeOutlook({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeOutlookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeTeams</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeTeams({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeTeamsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeFathom</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Fathom OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeFathom({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeFathomRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeMonday</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Monday OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (space-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeMonday({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.OauthAuthorizeMondayRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeShopify</a>() -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.oauth.authorizeShopify();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `Oauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GoogleCloudOauth

<details><summary><code>client.googleCloudOauth.<a href="/src/api/resources/googleCloudOauth/client/Client.ts">authorizeGoogleCloud</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Google Cloud OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.googleCloudOauth.authorizeGoogleCloud({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeGoogleCloudRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GoogleCloudOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GoogleFormsOauth

<details><summary><code>client.googleFormsOauth.<a href="/src/api/resources/googleFormsOauth/client/Client.ts">authorizeGoogleForms</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Google Forms OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.googleFormsOauth.authorizeGoogleForms({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeGoogleFormsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GoogleFormsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## OnedriveOauth

<details><summary><code>client.onedriveOauth.<a href="/src/api/resources/onedriveOauth/client/Client.ts">refreshToken</a>({ ...params }) -> Klavis.AzureAdoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.onedriveOauth.refreshToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshTokenOauthOnedriveRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OnedriveOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## OutlookOauth

<details><summary><code>client.outlookOauth.<a href="/src/api/resources/outlookOauth/client/Client.ts">refreshToken</a>({ ...params }) -> Klavis.AzureAdoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.outlookOauth.refreshToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshTokenOauthOutlookRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OutlookOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## MscalendarOauth

<details><summary><code>client.mscalendarOauth.<a href="/src/api/resources/mscalendarOauth/client/Client.ts">authorizeMsCalendar</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mscalendarOauth.authorizeMsCalendar({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeMsCalendarRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MscalendarOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.mscalendarOauth.<a href="/src/api/resources/mscalendarOauth/client/Client.ts">refreshToken</a>({ ...params }) -> Klavis.AzureAdoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.mscalendarOauth.refreshToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshTokenOauthMscalendarRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MscalendarOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## TeamsOauth

<details><summary><code>client.teamsOauth.<a href="/src/api/resources/teamsOauth/client/Client.ts">refreshToken</a>({ ...params }) -> Klavis.AzureAdoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.teamsOauth.refreshToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshTokenOauthTeamsRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TeamsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## ZoomOauth

<details><summary><code>client.zoomOauth.<a href="/src/api/resources/zoomOauth/client/Client.ts">authorizeZoom</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.zoomOauth.authorizeZoom({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeZoomRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ZoomOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.zoomOauth.<a href="/src/api/resources/zoomOauth/client/Client.ts">refreshToken</a>({ ...params }) -> Klavis.ZoomOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.zoomOauth.refreshToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshTokenOauthZoomRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ZoomOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## ZohoMailOauth

<details><summary><code>client.zohoMailOauth.<a href="/src/api/resources/zohoMailOauth/client/Client.ts">authorizeZohoMail</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Zoho Mail OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- client_id: Optional client ID for white labeling
- scope: Optional scopes to request (comma-separated)
- redirect_url: Optional URL to redirect to after authorization completes
  </dd>
  </dl>
  </dd>
  </dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.zohoMailOauth.authorizeZohoMail({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeZohoMailRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ZohoMailOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## SharesightOauth

<details><summary><code>client.sharesightOauth.<a href="/src/api/resources/sharesightOauth/client/Client.ts">authorizeSharesight</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sharesightOauth.authorizeSharesight({
    instance_id: "instance_id",
    client_id: "client_id",
    scope: "scope",
    redirect_url: "redirect_url",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeSharesightRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SharesightOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sharesightOauth.<a href="/src/api/resources/sharesightOauth/client/Client.ts">refreshToken</a>({ ...params }) -> Klavis.SharesightOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sharesightOauth.refreshToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshTokenOauthSharesightRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SharesightOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## IntercomOauth

<details><summary><code>client.intercomOauth.<a href="/src/api/resources/intercomOauth/client/Client.ts">authorizeintercomOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.intercomOauth.authorizeintercomOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeintercomOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `IntercomOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.intercomOauth.<a href="/src/api/resources/intercomOauth/client/Client.ts">refreshIntercomOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.intercomOauth.refreshIntercomOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshIntercomOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `IntercomOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## PaypalOauth

<details><summary><code>client.paypalOauth.<a href="/src/api/resources/paypalOauth/client/Client.ts">authorizepaypalOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.paypalOauth.authorizepaypalOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizepaypalOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaypalOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.paypalOauth.<a href="/src/api/resources/paypalOauth/client/Client.ts">refreshPaypalOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.paypalOauth.refreshPaypalOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshPaypalOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaypalOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## SentryOauth

<details><summary><code>client.sentryOauth.<a href="/src/api/resources/sentryOauth/client/Client.ts">authorizesentryOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sentryOauth.authorizesentryOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizesentryOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SentryOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sentryOauth.<a href="/src/api/resources/sentryOauth/client/Client.ts">refreshSentryOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sentryOauth.refreshSentryOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshSentryOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SentryOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## NetlifyOauth

<details><summary><code>client.netlifyOauth.<a href="/src/api/resources/netlifyOauth/client/Client.ts">authorizenetlifyOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.netlifyOauth.authorizenetlifyOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizenetlifyOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NetlifyOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.netlifyOauth.<a href="/src/api/resources/netlifyOauth/client/Client.ts">refreshNetlifyOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.netlifyOauth.refreshNetlifyOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshNetlifyOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NetlifyOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## HuggingfaceOauth

<details><summary><code>client.huggingfaceOauth.<a href="/src/api/resources/huggingfaceOauth/client/Client.ts">authorizehuggingfaceOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.huggingfaceOauth.authorizehuggingfaceOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizehuggingfaceOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HuggingfaceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.huggingfaceOauth.<a href="/src/api/resources/huggingfaceOauth/client/Client.ts">refreshHuggingfaceOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.huggingfaceOauth.refreshHuggingfaceOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshHuggingfaceOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HuggingfaceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## SquareOauth

<details><summary><code>client.squareOauth.<a href="/src/api/resources/squareOauth/client/Client.ts">authorizesquareOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.squareOauth.authorizesquareOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizesquareOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SquareOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.squareOauth.<a href="/src/api/resources/squareOauth/client/Client.ts">refreshSquareOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.squareOauth.refreshSquareOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshSquareOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SquareOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## ClockwiseOauth

<details><summary><code>client.clockwiseOauth.<a href="/src/api/resources/clockwiseOauth/client/Client.ts">authorizeclockwiseOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.clockwiseOauth.authorizeclockwiseOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizeclockwiseOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClockwiseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.clockwiseOauth.<a href="/src/api/resources/clockwiseOauth/client/Client.ts">refreshClockwiseOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.clockwiseOauth.refreshClockwiseOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshClockwiseOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClockwiseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## JotformOauth

<details><summary><code>client.jotformOauth.<a href="/src/api/resources/jotformOauth/client/Client.ts">authorizejotformOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.jotformOauth.authorizejotformOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizejotformOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `JotformOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.jotformOauth.<a href="/src/api/resources/jotformOauth/client/Client.ts">refreshJotformOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.jotformOauth.refreshJotformOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshJotformOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `JotformOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## HoneycombOauth

<details><summary><code>client.honeycombOauth.<a href="/src/api/resources/honeycombOauth/client/Client.ts">authorizehoneycombOauth</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start OAuth flow and redirect to authorization page.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.honeycombOauth.authorizehoneycombOauth({
    instance_id: "instance_id",
    redirect_url: "redirect_url",
    force_refresh: true,
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.AuthorizehoneycombOauthRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HoneycombOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.honeycombOauth.<a href="/src/api/resources/honeycombOauth/client/Client.ts">refreshHoneycombOauthToken</a>({ ...params }) -> Klavis.McpoAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh OAuth token for an MCP connection.

This endpoint triggers a token refresh by making a list_tools request to the MCP server.
The MCP SDK will automatically detect if the token is expired and refresh it if a refresh_token is available.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.honeycombOauth.refreshHoneycombOauthToken({
    instance_id: "instance_id",
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Klavis.RefreshHoneycombOauthTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HoneycombOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Sandbox

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">createSandbox</a>(serverName) -> Klavis.CreateSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Acquire an idle sandbox instance for a specific MCP server. The sandbox will be marked as 'occupied'.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.createSandbox("jira");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**serverName:** `Klavis.SandboxMcpServer` — The MCP server name

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">getSandbox</a>(serverName, sandboxId) -> Klavis.SandboxInfo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve detailed information about a specific sandbox instance.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.getSandbox("jira", "sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**serverName:** `Klavis.SandboxMcpServer` — The MCP server name

</dd>
</dl>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">deleteSandbox</a>(serverName, sandboxId) -> Klavis.ReleaseSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Release an occupied sandbox back to idle state and marks the sandbox as available for reuse.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.deleteSandbox("jira", "sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**serverName:** `Klavis.SandboxMcpServer` — The MCP server name

</dd>
</dl>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">resetSandbox</a>(serverName, sandboxId) -> Klavis.ResetSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Reset the sandbox to its initial empty state, clearing all data while maintaining the sandbox instance.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.resetSandbox("jira", "sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**serverName:** `Klavis.SandboxMcpServer` — The MCP server name

</dd>
</dl>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeJiraSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with jira-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeJiraSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.JiraDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpJiraSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseJiraData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpJiraSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGoogleCalendarSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with google_calendar-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGoogleCalendarSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GoogleCalendarDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGoogleCalendarSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGoogleCalendarData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGoogleCalendarSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGmailSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with gmail-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGmailSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GmailData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGmailSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGmailData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGmailSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGoogleDocsSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with google_docs-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGoogleDocsSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GoogleDocsData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGoogleDocsSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGoogleDocsData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGoogleDocsSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGoogleDriveSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with google_drive-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGoogleDriveSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GoogleDriveData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGoogleDriveSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGoogleDriveData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGoogleDriveSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGoogleFormsSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with google_forms-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGoogleFormsSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GoogleFormsDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGoogleFormsSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGoogleFormsData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGoogleFormsSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGoogleSheetsSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with google_sheets-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGoogleSheetsSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GoogleSheetsDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGoogleSheetsSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGoogleSheetsData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGoogleSheetsSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeSalesforceSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with salesforce-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeSalesforceSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.SalesforceData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpSalesforceSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseSalesforceData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpSalesforceSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeOnedriveSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with onedrive-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeOnedriveSandbox("sandbox_id", {
    root: {
        name: "name",
    },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.OneDriveDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpOnedriveSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseOneDriveData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpOnedriveSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeMicrosoftTeamsSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with microsoft_teams-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeMicrosoftTeamsSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.MsTeamsDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpMicrosoftTeamsSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseMsTeamsData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpMicrosoftTeamsSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeOutlookMailSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with outlook_mail-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeOutlookMailSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.OutlookMailData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpOutlookMailSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseOutlookMailData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpOutlookMailSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeCalcomSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with Cal.com-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeCalcomSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.CalcomDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpCalcomSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseCalcomData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpCalcomSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeHubspotSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with hubspot-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeHubspotSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.HubSpotDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpHubspotSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseHubSpotData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpHubspotSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeQuickbooksSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with quickbooks-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeQuickbooksSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.QuickBooksData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpQuickbooksSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseQuickBooksData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpQuickbooksSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeMoneybirdSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with moneybird-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeMoneybirdSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.MoneybirdDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpMoneybirdSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseMoneybirdData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpMoneybirdSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeDropboxSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with dropbox-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeDropboxSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.DropboxData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpDropboxSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseDropboxData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpDropboxSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeShopifySandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with shopify-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeShopifySandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.ShopifyDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpShopifySandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseShopifyData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpShopifySandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeOutlookCalendarSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with outlook_calendar-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeOutlookCalendarSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.OutlookCalendarData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpOutlookCalendarSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseOutlookCalendarData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpOutlookCalendarSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeClickupSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with clickup-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeClickupSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.ClickUpDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpClickupSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseClickUpData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpClickupSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeCloseSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with close-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeCloseSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.CloseDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpCloseSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseCloseData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpCloseSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeResendSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with resend-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeResendSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.ResendDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpResendSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseResendData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpResendSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeWordpressSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with wordpress-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeWordpressSandbox("sandbox_id", {});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.WordPressData`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpWordpressSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseWordPressData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpWordpressSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeAsanaSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with asana-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeAsanaSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.AsanaDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpAsanaSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseAsanaData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpAsanaSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeMem0Sandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with mem0-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeMem0Sandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.Mem0DataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpMem0Sandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseMem0Data</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpMem0Sandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeSupabaseSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with supabase-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeSupabaseSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.SupabaseDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpSupabaseSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseSupabaseData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpSupabaseSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGithubSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with github-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGithubSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GitHubDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGithubSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGitHubData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGithubSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeLinearSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with linear-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeLinearSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.LinearDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpLinearSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseLinearData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpLinearSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeNotionSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with notion-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeNotionSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.NotionDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpNotionSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseNotionData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpNotionSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeSlackSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with slack-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeSlackSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.SlackDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpSlackSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseSlackData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpSlackSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeConfluenceSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with confluence-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeConfluenceSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.ConfluenceDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpConfluenceSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseConfluenceData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpConfluenceSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeDiscordSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with discord-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeDiscordSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.DiscordDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpDiscordSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseDiscordData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpDiscordSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeAirtableSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with airtable-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeAirtableSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.AirtableDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpAirtableSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseAirtableData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpAirtableSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeSnowflakeSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with snowflake-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeSnowflakeSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.SnowflakeDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpSnowflakeSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseSnowflakeData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpSnowflakeSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeGoogleCloudSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with google_cloud-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeGoogleCloudSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.GoogleCloudDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpGoogleCloudSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseGoogleCloudData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpGoogleCloudSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeMondaySandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with monday-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeMondaySandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.MondayDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpMondaySandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseMondayData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpMondaySandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">initializeMotionSandbox</a>(sandboxId, { ...params }) -> Klavis.InitializeSandboxResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Initialize the sandbox with motion-specific data following the defined schema.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.initializeMotionSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**request:** `Klavis.MotionDataInput`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="/src/api/resources/sandbox/client/Client.ts">dumpMotionSandbox</a>(sandboxId) -> Klavis.DumpSandboxResponseMotionData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from the sandbox in the same format used for initialization.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.sandbox.dumpMotionSandbox("sandbox_id");
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sandboxId:** `string` — The unique sandbox identifier

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `Sandbox.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>
