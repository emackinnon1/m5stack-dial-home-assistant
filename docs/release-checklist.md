# Open Source Release Checklist

Before publishing to GitHub, Hackster, or a ZIP download:

- [ ] Confirm `secrets.yaml` is not included.
- [ ] Confirm `.esphome/`, `esphome-env/`, `.venv/`, `.vscode/`, and `mini_code/` are not included.
- [ ] Run a sensitive scan for Wi-Fi names, passwords, API keys, local IPs, and local paths.
- [ ] Check that public Git commit author name/email are OK to publish.
- [ ] Replace local Home Assistant entities in `src/main/entities.yaml` with placeholders or examples.
- [ ] Run `esphome config dial.yaml` using placeholder secrets.
- [ ] Run `esphome compile dial.yaml` with the version pinned in `requirements.txt`.
- [ ] On a Dial, test music controls, HA metadata fallback, pause/resume and server disconnect/reconnect with and without Sendspin.
- [ ] Verify 100 x 100 artwork, 200 ms fade-out / 300 ms fade-in, rapid track changes and placeholder restoration on stream clear.
- [ ] Monitor free heap and responsiveness during repeated artwork updates on the no-PSRAM Dial.
- [ ] Add photos, demo GIFs, and setup notes for the community post.
- [ ] Keep third-party license notices for copied components, fonts, and icons.
- [ ] Publish from a fresh Git repository or a clean export folder, not from old history that may contain secrets.
