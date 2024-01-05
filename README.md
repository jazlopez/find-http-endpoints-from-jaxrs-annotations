# find-http-endpoints-from-jaxrs-annotations
The following program will scan the entry point directory for java files where HTTP endpoints are declared (using JAXRS annotations) 

### Download

Download the file upon your OS and rename to `find-http-endpoints-from-jaxrs-annotations`

```sh
# If Linux
mv find-http-endpoints-from-jaxrs-annotations-linux find-http-endpoints-from-jaxrs-annotations

# if OSX
mv find-http-endpoints-from-jaxrs-annotations-osx find-http-endpoints-from-jaxrs-annotations
```

### Permissions

Adjust permission accordingly

```
chmod +x find-http-endpoints-from-jaxrs-annotations
```

### Usage
```sh

./find-http-endpoints-from-jaxrs-annotations --entry-point /src/to/codebase

```

### Output
```
-------------------------------------------------------------------------------
The following program will scan the entry point directory for java files
where HTTP endpoints are declared (using JAXRS annotations) and will
output the declared endpoints wih its respective HTTP method.

Author: Jaziel Lopez <jazlopez at github.com> jlopez.mx
--------------------------------------------------------------------------------

Scanning: /src/to/codebase

--------------------------------------------------------------------------------
@POST
@Path("/v1/auth/loginUrl")

@Path("/v2")
	|-  @GET
	|-  @Path("/healthcheck")

@Path("/v2/sns/antivirus")
	|-  @POST
	|-  @Path("/handleFindings")

@Path("/v2/sns")
	|-  @POST
	|-  @Path("/processSnsMessage")
 ```
