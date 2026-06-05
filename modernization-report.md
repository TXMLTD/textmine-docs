# Documentation Modernization Report

## What changed

- Created a current-product docs structure around Workbench, Vault, Legislate, Workflows, Integrations, Playbooks, Records, Agents, Scribe, and Administration.
- Added generated pages for Legislate, Workbench MCP providers, and the hosted TextMine MCP server based on current frontend/backend code.
- Preserved all imported Intercom screenshots under `/images/intercom`.
- Preserved converted Intercom articles under `/archive/intercom` with a stale-content note.
- Added `llms.txt` so agents have a short map of the current docs.

## Code surfaces used as source

- `front-end/textmine-web-workspace/projects/textmine/web/src/app/routes/secured-routes/secured-routes.module.ts`
- `front-end/textmine-web-workspace/projects/textmine/web/src/app/pages/workflow/workflow-builder/workflow-builder.component.ts`
- `front-end/textmine-web-workspace/projects/textmine/web/src/app/pages/workflow/workflow-step.utils.ts`
- `front-end/textmine-web-workspace/projects/textmine/web/src/app/pages/business-records/business-records.component.ts`
- `front-end/textmine-web-workspace/projects/textmine/web/src/app/pages/playbook/playbook.component.ts`
- `front-end/textmine-web-workspace/projects/textmine/web/src/app/pages/workbench/workbench.component.ts`
- `front-end/textmine-web-workspace/projects/textmine/web/src/app/core/services/integration-providers.service.ts`
- `back-end/services/api/shared/src/main/java/com/legislate/api/workflow/dto/WorkflowActionType.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/workflow/dto/WorkflowTriggerTypeEnum.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/workbench/controller/WorkbenchController.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/workbench/service/task/WorkbenchTaskCapabilityRegistry.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/workbench/service/task/WorkbenchTaskExecutorImpl.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/integrations/providers/IntegrationProvider.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/integrations/providers/FileStorageProvider.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/integrations/providers/DocumentProvider.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/integrations/providers/GoogleDriveDocumentProvider.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/integrations/providers/SharePointIntegrationProvider.java`
- `back-end/services/api/shared/src/main/java/com/legislate/api/integrations/providers/NotionDocumentProvider.java`
- `back-end/services/mcp/src/main/java/com/legislate/mcp/tools/*.java`
- `back-end/services/mcp/src/main/java/com/legislate/mcp/config/PublicApiClientConfig.java`
- `back-end/services/mcp/docs/adding-a-tool.md`

## Source caveats

- `back-end/services/mcp/docs/adding-a-tool.md` contains older authentication wording about a static `MCP_API_KEY`; the generated docs follow the current `PublicApiClientConfig` code, which forwards the caller's bearer Authorization header to Public API.

## Manual review still needed

- Capture fresh screenshots for the current Workbench, Workflow builder, Records, Playbooks, Vault, and Scribe pages.
- Decide whether to publish the Intercom archive publicly or keep it unlisted for migration traceability.
- Add detailed click-by-click tutorials after product owners confirm the current IA and terminology.
- Set up redirects from old Intercom article URLs to the new maintained pages.
