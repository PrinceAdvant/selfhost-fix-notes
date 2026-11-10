# Deploy webhooks from CI: a minimal and safe pattern

Sometimes you want CI to run tests first and only then deploy. A deploy webhook does that.

## The pattern

1. CI runs tests on push.
2. On success for the main branch, CI calls the deploy webhook URL.
3. The platform pulls, builds and deploys.

```
curl -fsS -X POST "$DEPLOY_HOOK_URL" -H "Authorization: Bearer $DEPLOY_TOKEN"
```

## Keep it safe

- Store the URL and token as CI secrets, never in the repository.
- Use a token scoped to one app, so a leak only affects that app.
- Rotate the token when a maintainer leaves.
- Make the call fail the pipeline (`-f`) so a broken deploy trigger is visible.

The Peon docs on [deploy webhooks and API](https://peon.sh/docs/webhooks-and-api) list the endpoints. [Peon](https://peon.sh/) is the open-source deployment platform I contribute to.
