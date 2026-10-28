# Thuis

Dashboard voor IKEA DIRIGERA-lampen, met deurbel (Aqara G410), meldingen, automatiseringen en een
wandtablet-modus. Deze repo bevat alleen kant-en-klare releases; de broncode is niet openbaar.

## Android-tablet

1. Installeer **Termux** en **Termux:Boot** via [F-Droid](https://f-droid.org/packages/com.termux/).
2. Open Termux en plak:

   ```bash
   curl -fsSL https://github.com/svandelaarschot/home-dashboard-releases/releases/latest/download/install-android.sh | bash
   ```

## Windows-pc (10 of 11)

Open **PowerShell** en plak:

```powershell
irm https://github.com/svandelaarschot/home-dashboard-releases/releases/latest/download/install-windows.ps1 | iex
```

Dit installeert ook de tray-app (melding en beeld als er wordt aangebeld). Verwijderen:

```powershell
& ([scriptblock]::Create((irm https://github.com/svandelaarschot/home-dashboard-releases/releases/latest/download/install-windows.ps1))) -Uninstall
```

**Tweede installatie ernaast** (bijv. om te testen naast een bestaande): zelfde regel met een andere poort:

```powershell
& ([scriptblock]::Create((irm https://github.com/svandelaarschot/home-dashboard-releases/releases/latest/download/install-windows.ps1))) -Port 8081
```

Die krijgt een eigen map, eigen poorten, snelkoppelingen en tray-app. Verwijderen: `-Port 8081 -Uninstall`.

## Daarna

De **installatiewizard** opent in de browser: IKEA-hub zoeken en koppelen, deurbel, meldingen op je
telefoon en het scherm. Verhuis je van een ander apparaat? Kies in de wizard **Snapshot importeren**
(exporteren via Instellingen → Snapshot op het oude apparaat).

Bijwerken: dezelfde regel nog eens. Je instellingen en opnames blijven bewaard.

© Stefan van de Laarschot. Alle rechten voorbehouden; zie LICENSE.txt in de release.