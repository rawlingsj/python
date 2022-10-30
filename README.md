# python

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/python/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/python/actions/workflows/release.yaml)

This is a minimal Python image based on Alpine, using Python apks available on the Alpine Community repositories (not built from source as of now).<br/><br/>While this image is being developed, we will stick to the latest stable Python version which at this moment is `3.10.7`. Supported versions in the long term are TBD.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/python:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `latest` | `sha256:f5af1d911f2a3bb9079b207e59a4cfe4ee785923dc48d11430d5f8324de7da99`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:f5af1d911f2a3bb9079b207e59a4cfe4ee785923dc48d11430d5f8324de7da99) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


## Usage

To try out the image, run:

```shell
docker run --rm cgr.dev/chainguard/python python -VV
```

Python version installed 
```
Python 3.10.7 (main, Sep 11 2022, 22:42:41) [GCC 12.1.1 20220630]
```

Pip Version installed 

```shell 
docker run --rm cgr.dev/chainguard/python pip -V
```

```shell
pip 22.2.2 from /usr/lib/python3.10/site-packages/pip (python 3.10)
```


## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/python:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/python:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/python"
      },
      "image": {
        "docker-manifest-digest": "sha256:f5af1d911f2a3bb9079b207e59a4cfe4ee785923dc48d11430d5f8324de7da99"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "b574a642b36fedf534cd5d5dacbab5b73c577dd9",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/python",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEQCIE907HWVhRqFFNaO//IkD3/r6q3zfy47dG0wOjUeHpAAAiA8oWc8YMCrfSFJmsHCjwjri5RVoW49pIbdHVkOKRjgOg==",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI1OGUyNWU0ZjY2ZWE4ZjZhOGYxNWMyOWZmZTZmN2Y3OGI0YjlmYTY1MzYyODVmZjAxODNhZWNiYzhhN2QxOWU4In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUURsWXlnMnJ0aEVnNWxEbWMwOTFPNkxqak42UHc3YzViUzNhc2YwYWpPK2l3SWdXeXg1aEdENnlvMDdXOGhoNzVFRXNOSWNrME45U1BPbk9MVkhLWUpzRU00PSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnhWRU5EUVhwRFowRjNTVUpCWjBsVlZWQkhhMVUwVVdaVkszZHdiMWhSZVZGb1EwZFdjM1pRV21ScmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFFVFhkTlJFbDRUWHBKZDFkb1kwNU5ha2w0VFVSTmQwMUVTWGxOZWtsM1YycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZ0V0dSR1VUbHJjbXh0YzBKdFMxZzNXVlZ5YTFVMWNVVmxiazl0ZFhZemNGTjJhVk1LWkRGWGNFbDJNblk0TURCV1VHMURjMG92YTB3eE9UQldaMWRRVDFObllsWjViRmx3VEM5c1UzbEllVmxYUm14WWJUWlBRMEZyT0hkblowcE1UVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZGZFhkSUNrNXNSVVJWVkhVeGFqVllNa0ZJVW10SEswWnJOR0pWZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJGQldVUldVakJTUVZGSUwwSkdOSGRZU1ZwaFlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d6UWpWa1IyaDJZbWs0ZFZveWJEQmhTRlpwVEROa2RtTnRkRzFpUnprelkzazVlVnBYZUd4WldFNXNURzVzYUdKWGVFRmpiVlp0Q21ONU9XOWFWMFpyWTNrNWRGbFhiSFZOUkd0SFEybHpSMEZSVVVKbk56aDNRVkZGUlVzeWFEQmtTRUo2VDJrNGRtUkhPWEphVnpSMVdWZE9NR0ZYT1hVS1kzazFibUZZVW05a1Ywb3hZekpXZVZreU9YVmtSMVoxWkVNMWFtSXlNSGRHWjFsTFMzZFpRa0pCUjBSMmVrRkNRV2RSU1dNeVRtOWFWMUl4WWtkVmR3cE9aMWxMUzNkWlFrSkJSMFIyZWtGQ1FYZFJiMWxxVlROT1IwVXlUa1JLYVUxNldtMWFWMUp0VGxSTk1Ga3lVVEZhUkZacldWZE9hVmxYU1RGWmFtTjZDbGw2VlROT01sSnJUMVJCWTBKbmIzSkNaMFZGUVZsUEwwMUJSVVZDUVRWRVkyMVdhR1JIVldkVmJWWnpXbGRHZWxwVVFXMUNaMjl5UW1kRlJVRlpUeThLVFVGRlJrSkNhR3BoUjBad1ltMWtNVmxZU210TVYyeDBXVmRrYkdONU9YZGxXRkp2WWpJMGQwaFJXVXRMZDFsQ1FrRkhSSFo2UVVKQ1oxRlFZMjFXYlFwamVUbHZXbGRHYTJONU9YUlpWMngxVFVsSFNrSm5iM0pDWjBWRlFXUmFOVUZuVVVOQ1NITkZaVkZDTTBGSVZVRkRSME5UT0VOb1V5OHlhRVl3WkVaeUNrbzBVMk5TVjJOWmNrSlpPWGQ2YWxOaVpXRTRTV2RaTW1JelNVRkJRVWRGU25Gdk1rZFJRVUZDUVUxQlVtcENSVUZwUWk5MGNrWkZkMDVaTnk5QmMzQUtiamw2Y2xCamRFaHhSRkZSVjBWamRsaFdPR1ZWYldwemVUVjZUbEZCU1dka1pURnFSbW8wVDBveE0zZENVbXRDWjIwMWFXRlZUbEZ3ZURrMWVuQnhlQXA2WlRKWmVqVk9XakZWZDNkRFoxbEpTMjlhU1hwcU1FVkJkMDFFV25kQmQxcEJTWGRGV0hFdmJVTXdjRVpxYjA5SmJsRjZOMU5vVjJOaGVsazFWMlUyQ2xWME1tNURXRk5vWkRSRmFVTllSRlZ2WVRoSlpUTmxZMWM0V0hreE5GbHplRk5yVDBGcVFuQk9jREZDWVhocloxcERiMjkzZDI5TE9ESjVLMUpHZWxBS1NDc3ZVRFpKU1hRMlVTOVdUa3d6Ykd4a1lXaFFlV1pVYzA0elYzcDZXbEpMVmxnd1VFVkpQUW90TFMwdExVVk9SQ0JEUlZKVVNVWkpRMEZVUlMwdExTMHRDZz09In19fX0=",
          "integratedTime": 1667096023,
          "logIndex": 6135243,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/python/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/python",
      "githubWorkflowSha": "b574a642b36fedf534cd5d5dacbab5b73c577dd9",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3353752923",
      "sha": "b574a642b36fedf534cd5d5dacbab5b73c577dd9"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

