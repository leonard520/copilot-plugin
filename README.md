# copilot-plugin

This repository provides GitHub Copilot CLI plugins for Java modernization scenarios:

- `modernize-java`: upgrade Java and Spring Boot projects.
- `modernize-azure-java`: migrate Java applications to Azure services and modern Java versions.

## Repository layout

- Marketplace definition: `.github/plugin/marketplace.json`
- Plugin manifests:
  - `plugins/modernize-java/.github/plugin/plugin.json`
  - `plugins/modernize-azure-java/.github/plugin/plugin.json`
- Agent definitions:
  - `plugins/modernize-java/agents/modernize-java.agent.md`
  - `plugins/modernize-azure-java/agents/modernize-azure-java.agent.md`

## Use this plugin marketplace in Copilot CLI

1. Add this repository marketplace:

   ```bash
   copilot plugin marketplace add <path-to-repo>/.github/plugin/marketplace.json
   ```

2. Verify marketplaces:

   ```bash
   copilot plugin marketplace list
   ```

3. Browse plugins in this marketplace:

   ```bash
   copilot plugin marketplace browse modernize-java-plugins
   ```

4. Install plugins:

   ```bash
   copilot plugin install modernize-java@modernize-java-plugins
   copilot plugin install modernize-azure-java@modernize-java-plugins
   ```

## Example usage in Copilot CLI

After installation, start Copilot CLI and use prompts such as:

- For Java upgrades:
  - `Upgrade this project to Java 21 and Spring Boot 3.2`
- For Azure modernization:
  - `Migrate this Java app to Azure services`

The installed plugin agents will handle planning and implementation steps for those requests.
