# @guardian/actions-cloudformation

A simple action to support Cloudformation deployments via Riffraff. This is
useful when you have not yet migrated to
[@guardian/cdk](https://github.com/guardian/cdk) and want to avoid manual
uploads.

The action takes a single Cloudformation file and creates a Riffraff deployment
for it.

Example usage:

```yaml
- uses: guardian/actions-cloudformation@v1
  with:
    app: example
    stack: some-stack
    templatePath: cloudformation/cfn.json
    guActionsRiffRaffRoleArn: ${{ secrets.GU_RIFF_RAFF_ROLE_ARN }}
```

**Manual uploads should be avoided for critical infrastructure!**