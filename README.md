# Docker Action

This action builds and publishes a Docker image to a specified registry. It also has support for pushing to a backup registry if the main registry is rate-limited.

## Inputs

- `docker_registry`: The Docker registry to push the image to.
- `docker_username`: The username for the Docker registry.
- `docker_password`: The password for the Docker registry.
- `docker_push_webhook`: The webhook to push the image to.
- `backup_registry`: The backup Docker registry to push the image to.
- `backup_username`: The username for the backup Docker registry.
- `backup_password`: The password for the backup Docker registry.
- `backup_push_webhook`: The webhook to push the image to the backup registry.

## Usage

```yaml
uses: TBXark/docker-action@master
with:
  docker_registry: ${{ secrets.DOCKER_REGISTRY }}
  docker_username: ${{ secrets.DOCKER_USERNAME }}
  docker_password: ${{ secrets.DOCKER_PASSWORD }}
  docker_push_webhook: ${{ secrets.DOCKER_PUSH_WEBHOOK }}
  backup_registry: ${{ secrets.BACKUP_REGISTRY }}
  backup_username: ${{ secrets.BACKUP_USERNAME }}
  backup_password: ${{ secrets.BACKUP_PASSWORD }}
  backup_push_webhook: ${{ secrets.BACKUP_PUSH_WEBHOOK }}
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
