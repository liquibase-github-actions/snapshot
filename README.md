# Liquibase Snapshot Action
Official GitHub Action to run Liquibase Snapshot in your GitHub Action Workflow. For more information on how snapshot works visit the [Official Liquibase Documentation](https://docs.liquibase.com/commands/home.html).
## Snapshot
Capture the current state of the database
## Usage
```yaml
steps:
- uses: actions/checkout@v3
- uses: liquibase-github-actions/snapshot@v4.19.0
  with:
    # The JDBC database connection URL
    # string
    # Required
    url: ""

    # 
    # string
    # Optional
    database: ""

    # The default catalog name to use for the database connection
    # string
    # Optional
    defaultCatalogName: ""

    # The default schema name to use for the database connection
    # string
    # Optional
    defaultSchemaName: ""

    # The JDBC driver class
    # string
    # Optional
    driver: ""

    # The JDBC driver properties file
    # string
    # Optional
    driverPropertiesFile: ""

    # Password to use to connect to the database
    # string
    # Optional
    password: ""

    # The schemas to snapshot
    # string
    # Optional
    schemas: ""

    # 
    # string
    # Optional
    snapshotControl: ""

    # Output format to use (JSON, YAML, or TXT)
    # string
    # Optional
    snapshotFormat: ""

    # Username to use to connect to the database
    # string
    # Optional
    username: ""

```

### Secrets
It is a good practice to protect your database credentials with [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

## Optional Liquibase Global Inputs
The liquibase snapshot action accepts all valid liquibase global options as optional parameters. A full list is available in the official [Liquibase Documentation](https://docs.liquibase.com/parameters/command-parameters.html).

### Example
```yaml
steps:
  - uses: actions/checkout@v3
  - uses: liquibase-github-actions/snapshot@v4.19.0
    with:
      url: ""
      headless: true
      licenseKey: ${{ secrets.LIQUIBASE_LICENSE_KEY }}
      logLevel: INFO
```

## Feedback and Issues
This action is automatically generated. Please submit all feedback and issues with the [generator repository](https://github.com/liquibase/github-action-generator/issues).
