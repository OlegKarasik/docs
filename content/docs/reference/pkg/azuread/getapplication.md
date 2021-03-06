
---
title: "GetApplication"
block_external_search_index: true
---



Use this data source to access information about an existing Application within Azure Active Directory.

> **NOTE:** If you're authenticating using a Service Principal then it must have permissions to both `Read and write all (or owned by) applications` and `Sign in and read user profile` within the `Windows Azure Active Directory` API.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azuread from "@pulumi/azuread";

const example = pulumi.output(azuread.getApplication({
    name: "My First AzureAD Application",
}, { async: true }));

export const azureAdObjectId = example.id;
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-azuread/blob/master/website/docs/d/application.html.markdown.





## Using GetApplication

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getApplication<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azuread/#GetApplicationArgs">GetApplicationArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azuread/#GetApplicationResult">GetApplicationResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_application(</span>name=None<span class="p">, </span>oauth2_permissions=None<span class="p">, </span>object_id=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupApplication<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/go/azuread/?tab=doc#GetApplicationArgs">GetApplicationArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/go/azuread/?tab=doc#LookupApplicationResult">LookupApplicationResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetApplication </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azuread/Pulumi.Azuread.GetApplicationResult.html">GetApplicationResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azuread/Pulumi.Azuread.GetApplicationArgs.html">GetApplicationArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Application within Azure Active Directory.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Oauth2Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">List&lt;Get<wbr>Application<wbr>Oauth2Permission<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Object<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the Object ID of the Application within Azure Active Directory.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Application within Azure Active Directory.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Oauth2Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">[]Get<wbr>Application<wbr>Oauth2Permission</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Object<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the Object ID of the Application within Azure Active Directory.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Application within Azure Active Directory.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>oauth2Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">Get<wbr>Application<wbr>Oauth2Permission[]?</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>object<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the Object ID of the Application within Azure Active Directory.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Application within Azure Active Directory.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>oauth2_<wbr>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">List[Get<wbr>Application<wbr>Oauth2Permission]</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>object_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the Object ID of the Application within Azure Active Directory.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetApplication Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>App<wbr>Roles</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationapprole">List&lt;Get<wbr>Application<wbr>App<wbr>Role&gt;</a></span>
    </dt>
    <dd>{{% md %}}A collection of `app_role` blocks as documented below. For more information https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/app-roles
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Application<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Application ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Available<wbr>To<wbr>Other<wbr>Tenants</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Azure AD Application available to other tenants?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Membership<wbr>Claims</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The `groups` claim issued in a user or OAuth 2.0 access token that the app expects.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Homepage</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Identifier<wbr>Uris</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of user-defined URI(s) that uniquely identify a Web application within it's Azure AD tenant, or within a verified custom domain if the application is multi-tenant.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Logout<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the logout page.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Oauth2Allow<wbr>Implicit<wbr>Flow</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Azure AD Application allow OAuth2.0 implicit flow tokens?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Oauth2Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">List&lt;Get<wbr>Application<wbr>Oauth2Permission&gt;</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Object<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Object ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Owners</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of User Object IDs that are assigned ownership of the application registration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Reply<wbr>Urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Required<wbr>Resource<wbr>Accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccess">List&lt;Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access&gt;</a></span>
    </dt>
    <dd>{{% md %}}A collection of `required_resource_access` blocks as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>App<wbr>Roles</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationapprole">[]Get<wbr>Application<wbr>App<wbr>Role</a></span>
    </dt>
    <dd>{{% md %}}A collection of `app_role` blocks as documented below. For more information https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/app-roles
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Application<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Application ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Available<wbr>To<wbr>Other<wbr>Tenants</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Azure AD Application available to other tenants?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Membership<wbr>Claims</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The `groups` claim issued in a user or OAuth 2.0 access token that the app expects.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Homepage</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Identifier<wbr>Uris</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of user-defined URI(s) that uniquely identify a Web application within it's Azure AD tenant, or within a verified custom domain if the application is multi-tenant.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Logout<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the logout page.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Oauth2Allow<wbr>Implicit<wbr>Flow</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Azure AD Application allow OAuth2.0 implicit flow tokens?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Oauth2Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">[]Get<wbr>Application<wbr>Oauth2Permission</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Object<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Object ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Owners</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of User Object IDs that are assigned ownership of the application registration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Reply<wbr>Urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Required<wbr>Resource<wbr>Accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccess">[]Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access</a></span>
    </dt>
    <dd>{{% md %}}A collection of `required_resource_access` blocks as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>app<wbr>Roles</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationapprole">Get<wbr>Application<wbr>App<wbr>Role[]</a></span>
    </dt>
    <dd>{{% md %}}A collection of `app_role` blocks as documented below. For more information https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/app-roles
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>application<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Application ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>available<wbr>To<wbr>Other<wbr>Tenants</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Is this Azure AD Application available to other tenants?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group<wbr>Membership<wbr>Claims</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The `groups` claim issued in a user or OAuth 2.0 access token that the app expects.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>homepage</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>identifier<wbr>Uris</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of user-defined URI(s) that uniquely identify a Web application within it's Azure AD tenant, or within a verified custom domain if the application is multi-tenant.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>logout<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the logout page.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>oauth2Allow<wbr>Implicit<wbr>Flow</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Does this Azure AD Application allow OAuth2.0 implicit flow tokens?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>oauth2Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">Get<wbr>Application<wbr>Oauth2Permission[]</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>object<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Object ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>owners</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of User Object IDs that are assigned ownership of the application registration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>reply<wbr>Urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>required<wbr>Resource<wbr>Accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccess">Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access[]</a></span>
    </dt>
    <dd>{{% md %}}A collection of `required_resource_access` blocks as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>app_<wbr>roles</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationapprole">List[Get<wbr>Application<wbr>App<wbr>Role]</a></span>
    </dt>
    <dd>{{% md %}}A collection of `app_role` blocks as documented below. For more information https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/app-roles
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>application_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}the Application ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>available_<wbr>to_<wbr>other_<wbr>tenants</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Azure AD Application available to other tenants?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group_<wbr>membership_<wbr>claims</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The `groups` claim issued in a user or OAuth 2.0 access token that the app expects.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>homepage</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>identifier_<wbr>uris</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of user-defined URI(s) that uniquely identify a Web application within it's Azure AD tenant, or within a verified custom domain if the application is multi-tenant.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>logout_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL of the logout page.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>oauth2_<wbr>allow_<wbr>implicit_<wbr>flow</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Azure AD Application allow OAuth2.0 implicit flow tokens?
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>oauth2_<wbr>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationoauth2permission">List[Get<wbr>Application<wbr>Oauth2Permission]</a></span>
    </dt>
    <dd>{{% md %}}A collection of OAuth 2.0 permission scopes that the web API (resource) app exposes to client apps. Each permission is covered by a `oauth2_permission` block as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>object_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}the Object ID of the Azure Active Directory Application.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>owners</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of User Object IDs that are assigned ownership of the application registration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>reply_<wbr>urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>required_<wbr>resource_<wbr>accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccess">List[Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access]</a></span>
    </dt>
    <dd>{{% md %}}A collection of `required_resource_access` blocks as documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types

<h4>Get<wbr>Application<wbr>App<wbr>Role</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/azuread/types/output/#GetApplicationAppRole">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/go/azuread/?tab=doc#GetApplicationAppRole">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Allowed<wbr>Member<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}Specifies whether this app role definition can be assigned to users and groups, or to other applications (that are accessing this application in daemon service scenarios). Possible values are: `User` and `Application`, or both.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Permission help text that appears in the admin app assignment and consent experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Display name for the permission that appears in the admin consent and app assignment experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Allowed<wbr>Member<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Specifies whether this app role definition can be assigned to users and groups, or to other applications (that are accessing this application in daemon service scenarios). Possible values are: `User` and `Application`, or both.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Permission help text that appears in the admin app assignment and consent experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Display name for the permission that appears in the admin consent and app assignment experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>allowed<wbr>Member<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Specifies whether this app role definition can be assigned to users and groups, or to other applications (that are accessing this application in daemon service scenarios). Possible values are: `User` and `Application`, or both.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Permission help text that appears in the admin app assignment and consent experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Display name for the permission that appears in the admin consent and app assignment experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>allowed<wbr>Member<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Specifies whether this app role definition can be assigned to users and groups, or to other applications (that are accessing this application in daemon service scenarios). Possible values are: `User` and `Application`, or both.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Permission help text that appears in the admin app assignment and consent experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>display_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Display name for the permission that appears in the admin consent and app assignment experiences.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Application<wbr>Oauth2Permission</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azuread/types/input/#GetApplicationOauth2Permission">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azuread/types/output/#GetApplicationOauth2Permission">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/go/azuread/?tab=doc#GetApplicationOauth2PermissionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/go/azuread/?tab=doc#GetApplicationOauth2Permission">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Admin<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Admin<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Admin<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Admin<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>admin<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>admin<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>admin<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>admin<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The display name of the admin consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>is<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines if the app role is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Consent<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Consent<wbr>Display<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The display name of the user consent
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the value of the roles claim that the application should expect in the authentication and access tokens.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/azuread/types/output/#GetApplicationRequiredResourceAccess">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/go/azuread/?tab=doc#GetApplicationRequiredResourceAccess">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccessresourceaccess">List&lt;Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access<wbr>Resource<wbr>Access<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A collection of `resource_access` blocks as documented below
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier for the resource that the application requires access to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccessresourceaccess">[]Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access<wbr>Resource<wbr>Access</a></span>
    </dt>
    <dd>{{% md %}}A collection of `resource_access` blocks as documented below
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier for the resource that the application requires access to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>Accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccessresourceaccess">Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access<wbr>Resource<wbr>Access[]</a></span>
    </dt>
    <dd>{{% md %}}A collection of `resource_access` blocks as documented below
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier for the resource that the application requires access to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>Accesses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getapplicationrequiredresourceaccessresourceaccess">List[Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access<wbr>Resource<wbr>Access]</a></span>
    </dt>
    <dd>{{% md %}}A collection of `resource_access` blocks as documented below
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique identifier for the resource that the application requires access to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Application<wbr>Required<wbr>Resource<wbr>Access<wbr>Resource<wbr>Access</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/azuread/types/output/#GetApplicationRequiredResourceAccessResourceAccess">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azuread/sdk/go/azuread/?tab=doc#GetApplicationRequiredResourceAccessResourceAccess">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique identifier of the `app_role`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the permission
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







