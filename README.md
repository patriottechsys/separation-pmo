# Separation PMO

## LLM API key

The app reads the Anthropic API key from the `ANTHROPIC_API_KEY` environment variable. It is optional: without it the AI features run in offline/fallback mode. The default model is `claude-sonnet-5-5` (override with `CLAUDE_MODEL`).

The key is the shared secret `Demo-Apps-Share-API-Key` in the Azure Key Vault `kv-demo-apps-shared` (subscription "Demo Apps"). Fetch it with:

```
az keyvault secret show --vault-name kv-demo-apps-shared --name Demo-Apps-Share-API-Key --subscription "Demo Apps" --query value -o tsv
```

Set it in a local `.env` file (see `.env.example`) or in the Render dashboard.
