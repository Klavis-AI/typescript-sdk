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

- servers: Can be 'ALL' to add all available Klavis MCP servers, a list of specific server names, or null to add no servers
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
- servers: Can be 'ALL' to delete all available Klavis MCP servers, a list of specific server names, or null to delete no servers
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
await client.mcpServer.deleteServersFromStrata("strataId");
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

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getStrataInstance</a>(strataId) -> Klavis.StrataGetResponse</code></summary>
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
await client.mcpServer.getStrataInstance("strataId");
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
await client.mcpServer.getServerInstance("instance_id");
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

**instanceId:** `string` — The ID of the connection instance whose status is being checked. This is returned by the Create API.

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
await client.mcpServer.deleteInstanceAuth("instance_id");
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
await client.mcpServer.deleteServerInstance("instance_id");
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
await client.mcpServer.getTools("Affinity");
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

Sets authentication data for a specific instance.
Accepts either API key authentication or general authentication data.
This updates the auth_metadata for the specified instance.

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

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getInstanceAuthData</a>(instanceId) -> Klavis.GetAuthDataResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves the auth data for a specific instance that the API key owner controls.
Includes access token, refresh token, and other authentication data.

This endpoint includes proper ownership verification to ensure users can only access
authentication data for instances they own. It also handles token refresh if needed.

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
await client.mcpServer.getInstanceAuthData("instance_id");
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

**instanceId:** `string` — The ID of the connection instance to get auth data for.

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

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getOauthUrl</a>({ ...params }) -> Klavis.GetOAuthUrlResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Gets the OAuth authorization URL for a specific MCP server and instance.
Returns the complete OAuth URL with the instance ID as a query parameter.

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
await client.mcpServer.getOauthUrl({
    serverName: "Affinity",
    instanceId: "instanceId",
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

**request:** `Klavis.GetOAuthUrlRequest`

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

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getServerInstancesByUser</a>({ ...params }) -> Klavis.GetServerInstancesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all MCP server instances information by user ID and platform name.

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
await client.user.getServerInstancesByUser({
    user_id: "user_id",
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

**request:** `Klavis.GetServerInstancesByUserRequest`

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
await client.user.deleteUserByUserId("user_id");
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

<details><summary><code>client.oauth.<a href="/src/api/resources/oauth/client/Client.ts">authorizeShopify</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Start Shopify OAuth flow

Parameters:

- instance_id: Identifier for the instance requesting authorization
- shop: Shopify shop domain (e.g., mystore.myshopify.com)
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
await client.oauth.authorizeShopify({
    instance_id: "instance_id",
    shop: "shop",
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

**request:** `Klavis.OauthAuthorizeShopifyRequest`

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
