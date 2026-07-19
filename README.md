# My custom Home Assistant Apps

This repository is designed to be easily integrated into any Home
Assistant instance via the Add-on Store.

## 🚀 Included Add-ons

* **[AppDaemon](https://www.appdaemon.org/)**: Official [base
  container](https://github.com/hassio-addons/app-appdaemon/) with
  `pymodbus`, `ruamel.yaml`, and `spotipy` pre-installed. This allows
  to boot the system fully even before the network link is up.

---

## 📥 How to install this repository

If you have *My Home Assistant* configured correctly, you can add this
collection of add-ons by clicking the button:

[![Open your Home Assistant instance and show the add app repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fjougs%2Fmy.ha-apps)

If that does not work, you have to run by following these steps:

1. Open your Home Assistant **Settings**.
2. Navigate to **Add-ons**.
3. Click the **Add-on Store** button in the bottom right.
4. Click the **three vertical dots** in the top right corner and
   select **Repositories**.
5. Copy and paste the following URL into the box:
   `[https://github.com/jougs/my.ha-apps](https://github.com/jougs/my.ha-apps)`
6. Click **Add**.

Once added, the page will refresh, and your custom add-ons will appear
at the bottom of the Add-on Store list.

---

## 🛠 For Developers / Modifying the Repository

This repository uses **GitHub Actions** to automatically build and
push multi-architecture Docker images (supporting `amd64` and `arm64`
for Raspberry Pi) to the **GitHub Container Registry (GHCR)**.

### Adding a new Add-on

1. Create a new directory in the root of this repo.
2. Add your `Dockerfile` and `config.yaml` to that directory.
3. Create a new `build-<yourappname>.yaml` under `.github/workflows/`
   to register your new folder for building and pushing.
4. Push your changes to the `main` branch.
5. **Important:** After the first successful build, go to the
   **Packages** section of this repository on GitHub and ensure your
   new package visibility is set to **Public**.
