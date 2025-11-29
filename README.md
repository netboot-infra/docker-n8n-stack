# Docker N8N Stack

## Format

To maintain a consistent structure across all Docker configuration files, I use the following command to reorganize and sort the contents of the docker-compose.yml file:

```bash
yq eval '.services |= with_entries(.value |= sort_keys(..))' *
```
