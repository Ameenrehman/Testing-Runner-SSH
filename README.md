# Testing-Runner-SSH

Interactive SSH debugging for GitHub Actions runners using Tailscale.

## How to Run
1. Ensure Tailscale is running on your local machine.
2. Ensure you have added the repository secrets:
   - `TS_OAUTH_CLIENT_ID`
   - `TS_OAUTH_SECRET`
3. Go to the **Actions** tab in GitHub and run the **Interactive SSH Debug (Tailscale)** workflow.
4. Check the workflow logs under "Wait for SSH Session" to get your SSH connection details.
5. Connect via:
   ```bash
   ssh runner@<tailscale-ip-or-hostname>
   ```
6. When done, end the session cleanly:
   ```bash
   touch /tmp/exit_session
   ```
