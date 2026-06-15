## 02.06.2026
### Tasks Completed:

- Completed an overview of Dukanify's Onboarding Backend.
    - Understood the overall onboarding workflow.
    - Understood the Database Schema.
    - Understood the API Endpoints.
    - Understood the Flow of the Backend.
    - Understood the Tech Stack used in the Backend.
- Studied PydanticAI retries and Celery retries
    - Agent retries are different from Celery task retries.
    - Understood the thin-line between Retries and Loops.
- Added a feature to fetch/scrape website themes and landing page designs using FireCrawl
    - Researched on how to use FireCrawl and integrate it with pydanticAI
    - Implemented the feature in the backend
    - Created a new endpoint to fetch the data
    - Tested using Postman to check the working of the feature

### Key Learnings

- Agent retries are independent of Celery task retries.
- FireCrawl can be integrated into onboarding workflows to extract website structure and design information.
- Understanding backend flow is easier when tracing requests from endpoint → service → model.

## 03.06.2026
### Tasks Completed

- Enhanced the FireCrawl-based competitor website analysis feature.
- Extended the scraping workflow to extract additional business context from competitor websites.
- Added support for fetching:
    - Executive Summary
    - Business Data
- Previously, the workflow extracted only brandkit-related information (CSS, styling, design assets, and theme data).
- Tested the updated implementation and validated the extracted data structure.

### Key Learnings

- Website scraping can be used to gather both visual branding information and business-level context.
- Expanding the extracted dataset improves the quality of information available for downstream onboarding workflows.
- Maintaining a consistent output structure becomes increasingly important as new data sources are added.

## 04.06.2026
### Tasks Completed

- Analyzed the website-builder architecture and its task execution workflow using monitoring tools.
- Evaluated the configuration schemas that define layout sections, component variants, and content variables.
- Explored how the configuration schemas steer the website generation process:
    - Level 2 (Section Selection): Uses section categories as validation constraints for the LLM to choose which section types to include on each page.
    - Level 3 (Component Selection): Resolves section categories to allowed component variants and dynamically forces the LLM to select exactly one valid variant per section.
    - Level 4 (Content Generation): Builds content-generation schemas based on the selected components, mapping static variables and grouping dynamic lists into simplified objects for the LLM before converting the final output back to the frontend format.

### Key Learnings:

- Decoupling website generation into distinct phases (Sections → Components → Content) enables strict validation at each level and improves model reliability.
- Restricting content fields to specific enums for images and links prevents the LLM from hallucinating dummy asset URLs.
- Translating complex frontend component schemas into simplified LLM schemas, and post-processing the output programmatically, reduces prompt complexity and input token overhead.