<table>
  <tr>
    <td width="150" rowspan="2">
      <a href="https://summerpearlgroup.gr" target="_blank">
        <img src="https://github.com/Stolichnayer/Summer-Pearl-Group-IDOR-XSS/raw/main/logo.png" alt="Summer Pearl Logo" width="120"/>
      </a>
    </td>
    <td>
      <h1>Summer Pearl Group</h1>
      <h3>Vacation Rental Management Platform Vulnerability</h3>
    </td>
  </tr>
  <tr>
    <td>
      <table>
        <tr>
          <td>
            🌐 <a href="https://summerpearlgroup.gr" target="_blank">Main Site</span></a>
          </td>
          <td style="padding-left: 15px;">
            🚀 <a href="https://summerpearlgroup.gr/spgpm/releases" target="_blank">Release Notes</span></a>
          </td>
        </tr>
      </table>
    </td>
  </tr>
</table>

## Broken Access Control Vulnerability

## 📜 Description
**Summer Pearl Group's Vacation Rental Management Platform** versions prior to **v1.0.2** suffer from insufficient server-side authorization (Broken Access Control, CWE‑284). Authenticated attackers can call several endpoints and perform create/update/delete actions on resources owned by arbitrary users by manipulating request parameters (e.g., owner or resource id). This allows unauthorized data manipulation (create/modify/delete listings, partners, guests, bookings) and may lead to data loss, integrity violations, and privacy breaches.

## 🔍 Affected Versions

| Status       | Version         |
|--------------|-----------------|
| 🔴 Vulnerable | ≤ `v1.0.1`     |
| 🟢  Fixed     | &nbsp;&nbsp;&nbsp; `v1.0.2`        |


## :triangular_flag_on_post: Vulnerable Endpoints


| **HTTP Method**        | **Endpoint**     |
|---------------|--------------|
| POST  | /spgpm/updateListing |
| DELETE  | /spgpm/deleteListing |
| POST | /spgpm/updatePartner |
| DELETE | /spgpm/deletePartner |
| POST  |/spgpm/updateGuest |
| POST | /updateBooking |
| DELETE  |/deleteBooking |

## ⚠️ Disclaimer
This project is intended for **educational and ethical research purposes only**. Unauthorized testing on systems without explicit permission is illegal. Use responsibly and only on systems you own or have permission to test.

## 🧑‍💻 Discovery
The vulnerability was discovered by **Alex Perrakis (Stolichnayer)**.

## 🔗 **References:**
- [Summer Pearl Group](https://summerpearlgroup.gr/spgpm/portal)
- [Vacation Rental Management Platform](https://summerpearlgroup.gr/spgpm/login)
- [Release v1.0.2 Notes (Patch)](https://summerpearlgroup.gr/spgpm/releases)

