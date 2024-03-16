# action-ssh-runner

Run ssh commands on remote server

```yaml
  deployment:
    name: 🌐 Deploy
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: alshdavid/action-ssh-runner@main
        with:
          ssh-private-key: "${{ secrets.APSE2_ALSHDAVID_C7G_LARGE_PEM }}"
          user: ec2-user
          host: url-to-host.com
          port: 22
          shell: zsh
          run: |
            echo "hello world"
```