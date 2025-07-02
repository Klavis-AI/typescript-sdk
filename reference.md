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
    platformName: "platformName",
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

Deletes authentication metadata for a specific server connection instance.

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

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getTools</a>(serverName) -> Klavis.GetToolsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get list of tool names for a specific MCP server.
Mainly used for querying metadata about the MCP server.

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

**serverName:** `Klavis.McpServerName` — The name of the target MCP server.

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

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">setInstanceAuthToken</a>({ ...params }) -> Klavis.StatusResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Sets an authentication token for a specific instance.
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
await client.mcpServer.setInstanceAuthToken({
    instanceId: "instanceId",
    authToken: "authToken",
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

**request:** `Klavis.SetAuthTokenRequest`

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

<details><summary><code>client.mcpServer.<a href="/src/api/resources/mcpServer/client/Client.ts">getOAuthUrl</a>({ ...params }) -> Klavis.GetOAuthUrlResponse</code></summary>
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
await client.mcpServer.getOAuthUrl({
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
    platform_name: "platform_name",
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

## SlackOauth

<details><summary><code>client.slackOauth.<a href="/src/api/resources/slackOauth/client/Client.ts">authorizeSlack</a>({ ...params }) -> unknown</code></summary>
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
await client.slackOauth.authorizeSlack({
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

**request:** `Klavis.AuthorizeSlackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SlackOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.slackOauth.<a href="/src/api/resources/slackOauth/client/Client.ts">slackOAuthCallback</a>({ ...params }) -> Klavis.SlackOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Slack OAuth authorization.

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
await client.slackOauth.slackOAuthCallback();
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

**request:** `Klavis.SlackOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SlackOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GithubOauth

<details><summary><code>client.githubOauth.<a href="/src/api/resources/githubOauth/client/Client.ts">authorizeGithub</a>({ ...params }) -> unknown</code></summary>
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
await client.githubOauth.authorizeGithub({
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

**request:** `Klavis.AuthorizeGithubRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GithubOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.githubOauth.<a href="/src/api/resources/githubOauth/client/Client.ts">githubOAuthCallback</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from GitHub OAuth authorization.

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
await client.githubOauth.githubOAuthCallback();
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

**request:** `Klavis.GithubOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GithubOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## SupabaseOauth

<details><summary><code>client.supabaseOauth.<a href="/src/api/resources/supabaseOauth/client/Client.ts">authorizeSupabase</a>({ ...params }) -> unknown</code></summary>
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
await client.supabaseOauth.authorizeSupabase({
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

**request:** `Klavis.AuthorizeSupabaseRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SupabaseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.supabaseOauth.<a href="/src/api/resources/supabaseOauth/client/Client.ts">supabaseOAuthCallback</a>({ ...params }) -> Klavis.SupabaseOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Supabase OAuth authorization.

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
await client.supabaseOauth.supabaseOAuthCallback();
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

**request:** `Klavis.SupabaseOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SupabaseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.supabaseOauth.<a href="/src/api/resources/supabaseOauth/client/Client.ts">refreshSupabaseToken</a>({ ...params }) -> Klavis.SupabaseOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Supabase access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.supabaseOauth.refreshSupabaseToken({
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

**request:** `Klavis.RefreshSupabaseTokenOauthSupabaseRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SupabaseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## NotionOauth

<details><summary><code>client.notionOauth.<a href="/src/api/resources/notionOauth/client/Client.ts">authorizeNotion</a>({ ...params }) -> unknown</code></summary>
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
await client.notionOauth.authorizeNotion({
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

**request:** `Klavis.AuthorizeNotionRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NotionOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.notionOauth.<a href="/src/api/resources/notionOauth/client/Client.ts">notionOAuthCallback</a>({ ...params }) -> Klavis.NotionOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Notion OAuth authorization.

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
await client.notionOauth.notionOAuthCallback();
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

**request:** `Klavis.NotionOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NotionOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## JiraOauth

<details><summary><code>client.jiraOauth.<a href="/src/api/resources/jiraOauth/client/Client.ts">authorizeJira</a>({ ...params }) -> unknown</code></summary>
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
await client.jiraOauth.authorizeJira({
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

**request:** `Klavis.AuthorizeJiraRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `JiraOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.jiraOauth.<a href="/src/api/resources/jiraOauth/client/Client.ts">jiraOAuthCallback</a>({ ...params }) -> Klavis.JiraOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Jira OAuth authorization.

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
await client.jiraOauth.jiraOAuthCallback();
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

**request:** `Klavis.JiraOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `JiraOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.jiraOauth.<a href="/src/api/resources/jiraOauth/client/Client.ts">refreshJiraToken</a>({ ...params }) -> Klavis.JiraOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Jira access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.jiraOauth.refreshJiraToken({
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

**request:** `Klavis.RefreshJiraTokenOauthJiraRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `JiraOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## ConfluenceOauth

<details><summary><code>client.confluenceOauth.<a href="/src/api/resources/confluenceOauth/client/Client.ts">authorizeConfluence</a>({ ...params }) -> unknown</code></summary>
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
await client.confluenceOauth.authorizeConfluence({
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

**request:** `Klavis.AuthorizeConfluenceRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConfluenceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.confluenceOauth.<a href="/src/api/resources/confluenceOauth/client/Client.ts">confluenceOAuthCallback</a>({ ...params }) -> Klavis.ConfluenceOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Confluence OAuth authorization.

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
await client.confluenceOauth.confluenceOAuthCallback();
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

**request:** `Klavis.ConfluenceOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConfluenceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.confluenceOauth.<a href="/src/api/resources/confluenceOauth/client/Client.ts">refreshConfluenceToken</a>({ ...params }) -> Klavis.ConfluenceOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Confluence access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.confluenceOauth.refreshConfluenceToken({
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

**request:** `Klavis.RefreshConfluenceTokenOauthConfluenceRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConfluenceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## WordpressOauth

<details><summary><code>client.wordpressOauth.<a href="/src/api/resources/wordpressOauth/client/Client.ts">authorizeWordpress</a>({ ...params }) -> unknown</code></summary>
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
await client.wordpressOauth.authorizeWordpress({
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

**request:** `Klavis.AuthorizeWordpressRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WordpressOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.wordpressOauth.<a href="/src/api/resources/wordpressOauth/client/Client.ts">wordpressOAuthCallback</a>({ ...params }) -> Klavis.WordPressOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from WordPress OAuth authorization.

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
await client.wordpressOauth.wordpressOAuthCallback();
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

**request:** `Klavis.WordpressOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WordpressOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GmailOauth

<details><summary><code>client.gmailOauth.<a href="/src/api/resources/gmailOauth/client/Client.ts">authorizeGmail</a>({ ...params }) -> unknown</code></summary>
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
await client.gmailOauth.authorizeGmail({
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

**request:** `Klavis.AuthorizeGmailRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GmailOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gmailOauth.<a href="/src/api/resources/gmailOauth/client/Client.ts">gmailOAuthCallback</a>({ ...params }) -> Klavis.GmailOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Gmail OAuth authorization.

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
await client.gmailOauth.gmailOAuthCallback();
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

**request:** `Klavis.GmailOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GmailOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gmailOauth.<a href="/src/api/resources/gmailOauth/client/Client.ts">refreshGmailToken</a>({ ...params }) -> Klavis.GmailOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Gmail access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.gmailOauth.refreshGmailToken({
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

**request:** `Klavis.RefreshGmailTokenOauthGmailRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GmailOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GdriveOauth

<details><summary><code>client.gdriveOauth.<a href="/src/api/resources/gdriveOauth/client/Client.ts">authorizeGDrive</a>({ ...params }) -> unknown</code></summary>
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
await client.gdriveOauth.authorizeGDrive({
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

**request:** `Klavis.AuthorizeGDriveRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GdriveOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gdriveOauth.<a href="/src/api/resources/gdriveOauth/client/Client.ts">gdriveOAuthCallback</a>({ ...params }) -> Klavis.GDriveOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Google Drive OAuth authorization.

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
await client.gdriveOauth.gdriveOAuthCallback();
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

**request:** `Klavis.GdriveOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GdriveOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gdriveOauth.<a href="/src/api/resources/gdriveOauth/client/Client.ts">refreshGdriveToken</a>({ ...params }) -> Klavis.GDriveOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Google Drive access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.gdriveOauth.refreshGdriveToken({
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

**request:** `Klavis.RefreshGdriveTokenOauthGdriveRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GdriveOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gdriveOauth.<a href="/src/api/resources/gdriveOauth/client/Client.ts">gdrivePickerPage</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Serve the Google Drive picker page with the appropriate credentials

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
await client.gdriveOauth.gdrivePickerPage();
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

**request:** `Klavis.GdrivePickerPageRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GdriveOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GcalendarOauth

<details><summary><code>client.gcalendarOauth.<a href="/src/api/resources/gcalendarOauth/client/Client.ts">authorizeGCalendar</a>({ ...params }) -> unknown</code></summary>
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
await client.gcalendarOauth.authorizeGCalendar({
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

**request:** `Klavis.AuthorizeGCalendarRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GcalendarOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gcalendarOauth.<a href="/src/api/resources/gcalendarOauth/client/Client.ts">gcalendarOAuthCallback</a>({ ...params }) -> Klavis.GCalendarOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Google Calendar OAuth authorization.

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
await client.gcalendarOauth.gcalendarOAuthCallback();
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

**request:** `Klavis.GcalendarOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GcalendarOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gcalendarOauth.<a href="/src/api/resources/gcalendarOauth/client/Client.ts">refreshGcalendarToken</a>({ ...params }) -> Klavis.GCalendarOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Google Calendar access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.gcalendarOauth.refreshGcalendarToken({
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

**request:** `Klavis.RefreshGcalendarTokenOauthGcalendarRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GcalendarOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GsheetsOauth

<details><summary><code>client.gsheetsOauth.<a href="/src/api/resources/gsheetsOauth/client/Client.ts">authorizeGSheets</a>({ ...params }) -> unknown</code></summary>
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
await client.gsheetsOauth.authorizeGSheets({
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

**request:** `Klavis.AuthorizeGSheetsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GsheetsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gsheetsOauth.<a href="/src/api/resources/gsheetsOauth/client/Client.ts">gsheetsOAuthCallback</a>({ ...params }) -> Klavis.GSheetsOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Google Sheets OAuth authorization.

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
await client.gsheetsOauth.gsheetsOAuthCallback();
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

**request:** `Klavis.GsheetsOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GsheetsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gsheetsOauth.<a href="/src/api/resources/gsheetsOauth/client/Client.ts">refreshGsheetsToken</a>({ ...params }) -> Klavis.GSheetsOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Google Sheets access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.gsheetsOauth.refreshGsheetsToken({
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

**request:** `Klavis.RefreshGsheetsTokenOauthGsheetsRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GsheetsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## GdocsOauth

<details><summary><code>client.gdocsOauth.<a href="/src/api/resources/gdocsOauth/client/Client.ts">authorizeGDocs</a>({ ...params }) -> unknown</code></summary>
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
await client.gdocsOauth.authorizeGDocs({
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

**request:** `Klavis.AuthorizeGDocsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GdocsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gdocsOauth.<a href="/src/api/resources/gdocsOauth/client/Client.ts">gdocsOAuthCallback</a>({ ...params }) -> Klavis.GDocsOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Google Docs OAuth authorization.

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
await client.gdocsOauth.gdocsOAuthCallback();
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

**request:** `Klavis.GdocsOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GdocsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.gdocsOauth.<a href="/src/api/resources/gdocsOauth/client/Client.ts">refreshGdocsToken</a>({ ...params }) -> Klavis.GDocsOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Google Docs access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.gdocsOauth.refreshGdocsToken({
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

**request:** `Klavis.RefreshGdocsTokenOauthGdocsRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GdocsOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## AttioOauth

<details><summary><code>client.attioOauth.<a href="/src/api/resources/attioOauth/client/Client.ts">authorizeAttio</a>({ ...params }) -> unknown</code></summary>
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
await client.attioOauth.authorizeAttio({
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

**request:** `Klavis.AuthorizeAttioRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AttioOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.attioOauth.<a href="/src/api/resources/attioOauth/client/Client.ts">attioOAuthCallback</a>({ ...params }) -> Klavis.AttioOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Attio OAuth authorization.

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
await client.attioOauth.attioOAuthCallback();
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

**request:** `Klavis.AttioOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AttioOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## SalesforceOauth

<details><summary><code>client.salesforceOauth.<a href="/src/api/resources/salesforceOauth/client/Client.ts">authorizeSalesforce</a>({ ...params }) -> unknown</code></summary>
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
await client.salesforceOauth.authorizeSalesforce({
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

**request:** `Klavis.AuthorizeSalesforceRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SalesforceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.salesforceOauth.<a href="/src/api/resources/salesforceOauth/client/Client.ts">salesforceOAuthCallback</a>({ ...params }) -> Klavis.SalesforceOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Salesforce OAuth authorization.

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
await client.salesforceOauth.salesforceOAuthCallback();
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

**request:** `Klavis.SalesforceOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SalesforceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.salesforceOauth.<a href="/src/api/resources/salesforceOauth/client/Client.ts">refreshSalesforceToken</a>({ ...params }) -> Klavis.SalesforceOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Salesforce access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.salesforceOauth.refreshSalesforceToken({
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

**request:** `Klavis.RefreshSalesforceTokenOauthSalesforceRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SalesforceOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## AsanaOauth

<details><summary><code>client.asanaOauth.<a href="/src/api/resources/asanaOauth/client/Client.ts">authorizeAsana</a>({ ...params }) -> unknown</code></summary>
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
await client.asanaOauth.authorizeAsana({
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

**request:** `Klavis.AuthorizeAsanaRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AsanaOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.asanaOauth.<a href="/src/api/resources/asanaOauth/client/Client.ts">asanaOAuthCallback</a>({ ...params }) -> Klavis.AsanaOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Asana OAuth authorization.

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
await client.asanaOauth.asanaOAuthCallback();
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

**request:** `Klavis.AsanaOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AsanaOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.asanaOauth.<a href="/src/api/resources/asanaOauth/client/Client.ts">refreshAsanaToken</a>({ ...params }) -> Klavis.AsanaOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Asana access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.asanaOauth.refreshAsanaToken({
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

**request:** `Klavis.RefreshAsanaTokenOauthAsanaRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AsanaOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## LinearOauth

<details><summary><code>client.linearOauth.<a href="/src/api/resources/linearOauth/client/Client.ts">authorizeLinear</a>({ ...params }) -> unknown</code></summary>
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
await client.linearOauth.authorizeLinear({
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

**request:** `Klavis.AuthorizeLinearRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinearOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.linearOauth.<a href="/src/api/resources/linearOauth/client/Client.ts">linearOAuthCallback</a>({ ...params }) -> Klavis.LinearOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Linear OAuth authorization.

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
await client.linearOauth.linearOAuthCallback();
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

**request:** `Klavis.LinearOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LinearOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## CloseOauth

<details><summary><code>client.closeOauth.<a href="/src/api/resources/closeOauth/client/Client.ts">authorizeClose</a>({ ...params }) -> unknown</code></summary>
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
await client.closeOauth.authorizeClose({
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

**request:** `Klavis.AuthorizeCloseRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CloseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.closeOauth.<a href="/src/api/resources/closeOauth/client/Client.ts">closeOAuthCallback</a>({ ...params }) -> Klavis.CloseOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Close OAuth authorization.

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
await client.closeOauth.closeOAuthCallback();
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

**request:** `Klavis.CloseOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CloseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.closeOauth.<a href="/src/api/resources/closeOauth/client/Client.ts">refreshCloseToken</a>({ ...params }) -> Klavis.CloseOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Close access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.closeOauth.refreshCloseToken({
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

**request:** `Klavis.RefreshCloseTokenOauthCloseRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CloseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.closeOauth.<a href="/src/api/resources/closeOauth/client/Client.ts">revokeCloseToken</a>({ ...params }) -> Klavis.CloseOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke Close access and refresh tokens

Parameters:

- instance_id: Identifier for the instance requesting token revocation

Returns:

- Success response if token was revoked successfully, error response otherwise
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
await client.closeOauth.revokeCloseToken({
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

**request:** `Klavis.RevokeCloseTokenOauthCloseRevokePostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CloseOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## ClickupOauth

<details><summary><code>client.clickupOauth.<a href="/src/api/resources/clickupOauth/client/Client.ts">authorizeClickUp</a>({ ...params }) -> unknown</code></summary>
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
await client.clickupOauth.authorizeClickUp({
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

**request:** `Klavis.AuthorizeClickUpRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClickupOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.clickupOauth.<a href="/src/api/resources/clickupOauth/client/Client.ts">clickUpOAuthCallback</a>({ ...params }) -> Klavis.ClickUpOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from ClickUp OAuth authorization.

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
await client.clickupOauth.clickUpOAuthCallback();
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

**request:** `Klavis.ClickUpOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClickupOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## AirtableOauth

<details><summary><code>client.airtableOauth.<a href="/src/api/resources/airtableOauth/client/Client.ts">authorizeAirtable</a>({ ...params }) -> unknown</code></summary>
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
await client.airtableOauth.authorizeAirtable({
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

**request:** `Klavis.AuthorizeAirtableRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AirtableOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.airtableOauth.<a href="/src/api/resources/airtableOauth/client/Client.ts">airtableOAuthCallback</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from Airtable OAuth authorization.

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
await client.airtableOauth.airtableOAuthCallback();
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

**request:** `Klavis.AirtableOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AirtableOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.airtableOauth.<a href="/src/api/resources/airtableOauth/client/Client.ts">refreshAirtableToken</a>({ ...params }) -> Klavis.AirtableOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired Airtable access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.airtableOauth.refreshAirtableToken({
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

**request:** `Klavis.RefreshAirtableTokenOauthAirtableRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AirtableOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## HubspotOauth

<details><summary><code>client.hubspotOauth.<a href="/src/api/resources/hubspotOauth/client/Client.ts">authorizeHubspot</a>({ ...params }) -> unknown</code></summary>
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
await client.hubspotOauth.authorizeHubspot({
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

**request:** `Klavis.AuthorizeHubspotRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HubspotOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.hubspotOauth.<a href="/src/api/resources/hubspotOauth/client/Client.ts">hubspotOAuthCallback</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Handles the callback from HubSpot OAuth authorization.

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
await client.hubspotOauth.hubspotOAuthCallback();
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

**request:** `Klavis.HubspotOAuthCallbackRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HubspotOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.hubspotOauth.<a href="/src/api/resources/hubspotOauth/client/Client.ts">refreshHubspotToken</a>({ ...params }) -> Klavis.HubSpotOAuthSuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Refresh an expired HubSpot access token using the stored refresh token

Parameters:

- instance_id: Identifier for the instance requesting token refresh

Returns:

- Success response if token was refreshed successfully, error response otherwise
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
await client.hubspotOauth.refreshHubspotToken({
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

**request:** `Klavis.RefreshHubspotTokenOauthHubspotRefreshTokenPostRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `HubspotOauth.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>
