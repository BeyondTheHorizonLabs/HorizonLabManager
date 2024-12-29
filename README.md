# Horizon Lab Manager (HLM)

**Horizon Lab Manager (HLM)** is a cutting-edge web-based application designed to streamline the management and maintenance of experiments in paranormal activity research, UAP phenomena studies, and advanced scientific exploration. Built with **Node.js** and **React.js**, HLM offers a user-friendly interface, robust integration capabilities, and future-proof scalability for managing and analyzing experiments.

---

## Features

- **Experiment Management**:
  - Create, manage, and monitor experiments in real-time.
  - Detailed logging of experiment metadata, results, and anomalies.
- **User Management**:
  - Role-based access control.
  - Integration with relational databases (SQLite, PostgreSQL, MySQL, Microsoft SQL Server).
  - Future support for SSO with Google and Microsoft.
- **Seamless Integration**:
  - Ties into Beyond The Horizon Labs' ecosystem:
    - **EctoProbe**: For visualizing and analyzing collected data.
    - **ParaSenseHub**: For aggregating sensor data.
    - **PhantomDroneOne**: For managing drone telemetry and anomalies.
    - **SkinwalkerPi** and **SkinwalkerOS**: For field device integration.
  - Centralized logging with OpenSearch, Elasticsearch, and other supported systems.
- **Advanced Reporting**:
  - Generate reports on experiment outcomes and trends.
  - Export data for deeper analysis in external tools.
- **Future-Proof Design**:
  - Modular architecture for integrating additional devices and tools.
  - Ready for machine learning and AI-driven insights.

---

## Prerequisites

- **System Requirements**:
  - Node.js 18 or later
  - A relational database (SQLite, PostgreSQL, MySQL, or Microsoft SQL Server)
  - Optional: Redis for caching
- **Additional Tools**:
  - Git for cloning the repository
  - A modern web browser for accessing the application

---

## Installation

### Clone the Repository

```bash
git clone git@github.com:BeyondTheHorizonLabs/HorizonLabManager.git
cd HorizonLabManager
```

### Install Dependencies

```bash
npm install
```

### Configure the Application

Edit the `config.json` file to set up the database connection and integration settings:

```json
{
  "database": {
    "type": "postgresql",
    "host": "localhost",
    "port": 5432,
    "username": "user",
    "password": "password",
    "database": "hlm_db"
  },
  "sso": {
    "google": {
      "clientId": "your-google-client-id",
      "clientSecret": "your-google-client-secret"
    },
    "microsoft": {
      "clientId": "your-microsoft-client-id",
      "clientSecret": "your-microsoft-client-secret"
    }
  },
  "port": 4000
}
```

### Start the Application

```bash
npm start
```

Access the application at [http://localhost:4000](http://localhost:4000).

---

## Integration with Other Apps

HLM is designed to integrate seamlessly with the Beyond The Horizon Labs ecosystem:

1. **EctoProbe**:
   - HLM will push experiment data to EctoProbe for advanced visualization and administration.
   - Use EctoProbe to view real-time experiment trends and anomalies.

2. **ParaSenseHub**:
   - Aggregate sensor data from multiple devices and link it to specific experiments managed by HLM.

3. **PhantomDroneOne**:
   - Incorporate drone telemetry data into experiment logs for detailed analysis of environmental conditions.

4. **SkinwalkerPi/SkinwalkerOS**:
   - Deploy HLM-compatible field devices to capture experiment data and sync with HLM.

### Configuration

Update each application’s configuration to include HLM as a central data manager. For example, in EctoProbe’s `config.json`:

```json
{
  "horizonLabManager": {
    "url": "http://hlm-server:4000",
    "apiKey": "your-api-key"
  }
}
```

---

## Contribution

We welcome contributions to Horizon Lab Manager! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or fix:

   ```bash
   git checkout -b feature-name
   ```

3. Commit your changes with clear messages:

   ```bash
   git commit -m "Add feature or fix description"
   ```

4. Push to your fork and submit a pull request.

For detailed guidelines, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

This project is licensed under the [MIT License](LICENSE).
