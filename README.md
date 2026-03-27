# Databricks ML Project using Databricks Asset Bundles

### A starter template for a Databricks-focused machine learning workflow.

## Databricks ML Project Layout
![Databricks ML project layout](https://github.com/KalyanbrataMaity/ml-dab-project/blob/main/assets/dab-ml-layout.png)

➤ 𝐂𝐨𝐧𝐟𝐢𝐠𝐮𝐫𝐚𝐭𝐢𝐨𝐧

→ 𝐝𝐚𝐭𝐚𝐛𝐫𝐢𝐜𝐤𝐬.𝐲𝐦𝐥 - your bundle config with variables and targets (dev, staging, prod)
→ 𝐩𝐲𝐩𝐫𝐨𝐣𝐞𝐜𝐭.𝐭𝐨𝐦𝐥 - package definition and dependencies

-

➤ 𝐎𝐫𝐜𝐡𝐞𝐬𝐭𝐫𝐚𝐭𝐢𝐨𝐧

Two folders that work together:

→ 𝐫𝐞𝐬𝐨𝐮𝐫𝐜𝐞𝐬/ - contains the 𝐃𝐀𝐁 job definitions as YAML files. They describe what runs, when, and on which cluster.

→ 𝐣𝐨𝐛𝐬/ - contains the actual Python scripts that those YAMLs point to. This is the code that gets executed.

👉 The key here: 𝐞𝐚𝐜𝐡 𝐣𝐨𝐛 𝐬𝐜𝐫𝐢𝐩𝐭 𝐢𝐬 𝐭𝐡𝐢𝐧. It imports everything from the core package and just orchestrates the steps. No business logic lives here.

-

➤ 𝐄𝐱𝐩𝐥𝐨𝐫𝐚𝐭𝐢𝐨𝐧

This is the sandbox, so nothing in this folder runs in production. Ever.

→ 𝐧𝐨𝐭𝐞𝐛𝐨𝐨𝐤𝐬/ - is exclusively for EDA, prototyping, and quick experiments.

-

➤ 𝐐𝐮𝐚𝐥𝐢𝐭𝐲

→ 𝐭𝐞𝐬𝐭𝐬/ - with three sections: unit tests, integration tests, and fixtures for sample data and mock configs.

If the core logic isn't properly tested, it doesn't get deployed. Simple as that.

-

 ➤ 𝐂𝐨𝐫𝐞 𝐥𝐨𝐠𝐢𝐜

→ 𝐬𝐫𝐜/𝐩𝐚𝐜𝐤𝐚𝐠𝐞_𝐧𝐚𝐦𝐞/ - is a proper installable Python library.

Ingestion, processing, feature engineering, training logic, etc. all structured as modules inside this package.

𝐖𝐞 𝐢𝐧𝐬𝐭𝐚𝐥𝐥 𝐢𝐭 𝐚𝐬 𝐚 𝐝𝐞𝐩𝐞𝐧𝐝𝐞𝐧𝐜𝐲 𝐟𝐨𝐫 𝐞𝐯𝐞𝐫𝐲 𝐬𝐢𝐧𝐠𝐥𝐞 𝐣𝐨𝐛 𝐰𝐞 𝐫𝐮𝐧. Training, evaluation, deployment, etc. they all import from the same tested, versioned codebase.
