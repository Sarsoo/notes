
```bash
terraform plan -out out.plan
terraform show -json | jq .resource_changes
rm out.plan
```

# Count
```bash
terraform show -json out.plan | jq '.resource_changes | length'
```