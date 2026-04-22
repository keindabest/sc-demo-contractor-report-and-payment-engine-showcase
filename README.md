# Audit-Friendly Contractor Payment Engine

Manual contractor payout packets usually fail on operations: too many handoffs, too much spreadsheet drift, and weak evidence consistency. This demo shows a Jira-gated workflow that validates context first, then generates payout documents in one controlled run.

**Typical transformation: 1 to 3 hours of manual prep per contractor packet -> under 10 minutes in one guided run.**

![Hero section](assets/screenshots/hero_section.png)

## Key Capabilities
- One guided flow from selection to generated payout package.
- Hard validation gate before generation (no partial runs).
- Four-tab control model in one app: Generation, Contractor Registry, Customer Registry, Contractor Roles.
- Jira-linked context load before payout amount is accepted.
- Controlled allocation and checksum consistency to the cent.
- Multi-artifact output generation with archive-first folder handling.
- Direct traceability from selected input to output folder.

## Outcome Snapshot
<table width="100%">
  <colgroup>
    <col style="width: 36%;">
    <col style="width: 32%;">
    <col style="width: 32%;">
  </colgroup>
  <thead>
    <tr>
      <th align="left">Dimension</th>
      <th align="left">Before</th>
      <th align="left">After</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Packet prep time</td>
      <td>1 to 3 hours per contractor</td>
      <td>Under 10 minutes per contractor</td>
    </tr>
    <tr>
      <td>Compliance signal</td>
      <td>Inconsistent evidence quality</td>
      <td>0 bank/tax claims in a 6-month window</td>
    </tr>
    <tr>
      <td>Monthly throughput</td>
      <td>Limited by manual effort</td>
      <td>50+ contractors and about 200 to 500 generated docs</td>
    </tr>
    <tr>
      <td>Team load</td>
      <td>Repeated cross-team handoffs</td>
      <td>About 20% lower recurring finance/accounting effort</td>
    </tr>
    <tr>
      <td>Data control</td>
      <td>Spreadsheet edits in scattered places</td>
      <td>In-app control across 4 tabs</td>
    </tr>
  </tbody>
</table>

## Demo Access
<table width="100%">
  <thead>
    <tr>
      <th align="left" width="36%">Resource</th>
      <th align="left">Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Web Application</td>
      <td><a href="https://script.google.com/macros/s/AKfycbyrbdZGJvIlB6GStnnLtYaIi233pMD99_L1wYDOlCJvNbCe1Vcl7eDxJGbU5vUgXjJG/exec">Open Web Application</a></td>
    </tr>
    <tr>
      <td>Data Source (Google Sheets)</td>
      <td><a href="https://docs.google.com/spreadsheets/d/19PDr-R5DAtLRL1EVh2zVdjLidEXx9b3L1YQnxs5cfIg/edit?usp=sharing">Open Data Source</a></td>
    </tr>
    <tr>
      <td>Generated Output Folder (Google Drive)</td>
      <td><a href="https://drive.google.com/drive/folders/174NopgrVC9V-PW6uw1kxrGJDXHrzgslo">Open Output Folder</a></td>
    </tr>
    <tr>
      <td>Public Showcase Repository</td>
      <td><a href="https://github.com/keindabest/sc-demo-contractor-report-and-payment-engine-showcase">Open Public Showcase Repository</a></td>
    </tr>
  </tbody>
</table>

## Quick How to Try Demo
1. Open the deployed application.
2. Select contractor, customer, month, and year.
3. Click Jira sync to load validated context.
4. Click `Create Documents`.
5. Open the Drive folder and inspect generated packet files.

## Demo Documentation Map

- Start here: [OVERVIEW](OVERVIEW.md) -> [DEMO_FLOW](DEMO_FLOW.md) -> [FILES](FILES.md)
- [FEATURES](FEATURES.md)
- [ARCHITECTURE](ARCHITECTURE.md)
- [USE_CASES](USE_CASES.md)
- [SECURITY_AND_DISCLOSURE](SECURITY_AND_DISCLOSURE.md)
- [DEPLOYMENT](DEPLOYMENT.md)
- [LICENSE](LICENSE)


## Disclosure (Short)

This is a sanitized public showcase. It includes synthetic screenshots and synthetic sample artifacts, and excludes secrets, private mappings, and internal orchestration details.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).

## Author

Daniel Kein

https://www.linkedin.com/in/daniel-kein/
