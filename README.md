# gramps-web-mcp-unraid

Unraid [Community Applications](https://forums.unraid.net/topic/38582-plug-in-community-applications/) templates for [gramps-web-mcp](https://github.com/Scormave/gramps-web-mcp).

## Templates

| Template | Image | Description |
|----------|-------|-------------|
| [gramps-web-mcp](templates/gramps-web-mcp.xml) | `ghcr.io/scormave/gramps-web-mcp:1.0.1` | MCP server for Gramps Web over HTTP |

## Prerequisites

- A running [Gramps Web](https://www.grampsweb.org/) instance with API credentials
- The `ghcr.io/scormave/gramps-web-mcp` package must be **public** on GitHub Container Registry so Unraid can pull it without authentication

## Manual test on Unraid

1. Docker → Add Container → **Template URL**:
   `https://raw.githubusercontent.com/Scormave/gramps-web-mcp-unraid/main/templates/gramps-web-mcp.xml`
2. Set `GRAMPS_API_URL`, `GRAMPS_USERNAME`, `GRAMPS_PASSWORD`, and `GRAMPS_TREE_ID`
3. Apply and confirm the container stays running
4. From another machine, connect an MCP client to `http://<unraid-host>:8080/mcp`

## Submit to Community Applications

1. Push this repository to a **public** GitHub repo
2. Open [ca.unraid.net/submit/new](https://ca.unraid.net/submit/new)
3. Sign in and enter your repository URL (e.g. `https://github.com/Scormave/gramps-web-mcp-unraid`)
4. Run **Validate**, then **Scan**
5. Fix any reported issues and submit for review

Official guides:

- [Builder guide](https://ca.unraid.net/submit/help/builders)
- [Repository XML format](https://ca.unraid.net/submit/help/repository-xml)
- [Repository info XML](https://ca.unraid.net/submit/help/repository-info-xml)

## Pre-submission checklist

- [ ] GitHub repository is public
- [ ] `ca_profile.xml` has a non-empty `<Profile>` section
- [ ] `TemplateURL` in each template points at the raw GitHub URL for that XML file on `main`
- [ ] `ghcr.io/scormave/gramps-web-mcp:1.0.1` is public and pullable
- [ ] Clean install tested on Unraid with valid Gramps Web credentials
- [ ] Validate and Scan pass in the submission portal

## Support

- Unraid install help: [forums support thread](https://forums.unraid.net/topic/199622-support-gramps-web-mcp-mcp-server-for-gramps-web-ai-genealogy)
- MCP server bugs and features: [gramps-web-mcp issues](https://github.com/Scormave/gramps-web-mcp/issues)
- Template issues: [gramps-web-mcp-unraid issues](https://github.com/Scormave/gramps-web-mcp-unraid/issues)

## License

MIT — see [LICENSE](LICENSE). The gramps-web-mcp container image is licensed separately under [AGPL-3.0](https://github.com/Scormave/gramps-web-mcp/blob/main/LICENSE).
