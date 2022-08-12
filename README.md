# action-s3-sandbox-cleanup
Removes merged deployments from the S3 sandbox directory

Example:
```
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
        with:
          fetch-depth: 0

      - uses: speareducation/action-s3-sandbox-cleanup
        env:
          AWS_ACCESS_KEY_ID: ${{ secrets.myKeyId }}
          AWS_SECRET_ACCESS_KEY: ${{ secrets.myKeySecret }}
          AWS_REGION: us-east-1
        with:
          s3-path: s3://my-bucket/project
```

