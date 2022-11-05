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
| `latest` | `sha256:7308f39cbf32df15835e2d9c4cac14167e9887759fcdc1978962ef188da2b697`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:7308f39cbf32df15835e2d9c4cac14167e9887759fcdc1978962ef188da2b697) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |


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
        "docker-manifest-digest": "sha256:7308f39cbf32df15835e2d9c4cac14167e9887759fcdc1978962ef188da2b697"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "d0a31b3a4bf455d290babb731caa5bea53344d4b",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/python",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEQCIEEfxCJXXD4O452lKp9TLNJuXivz2kggUUp5QeOxwAOxAiBDnWQaa6i4qH08USntzOyLrN8jC2qjs/vFQyU99prCww==",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJmZDRkMjNiNDkxZmJiMjdlYzdhMmVlNmY0MTFjMTlmNTA0MjVmYTBjZWZmZWJjODczNmI2ZDY4YmNkYzYzZTdjIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUURTVjRkNVY1OW5WZERNRkYxUlJoVmg2WEJ1MzRTZm04WW9Na1VSaEhNTVVRSWdUTDRSekYyc3RzTnN4TFRWQ2daczFOQ0JST21BalBhSjRUUTRiMGZlc1hVPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnhla05EUVhwSFowRjNTVUpCWjBsVlJFVXdNekV3VUVZd2RXWm1ZMVpZUW1kQk1IWTRiRUV3Y1hwUmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVUVRGTlJFVXhUa1JSZUZkb1kwNU5ha2w0VFZSQk1VMUVTWGRPUkZGNFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZMYmpOa05rMXhTM1UxUzFseVpIcEZhVFUxUVhCeWMzQkNPV2hvTkhSNk4yOVJkMWdLV1hvclRGUkVWVmgyVG05clZIZE5Ubk5aWm1vNWQyTjVMMGhHYVhSb1NVMXhVRUZ2YjJOc2NHWldTbWhSVW1VMGRuRlBRMEZzUVhkblowcE5UVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlV3WlUweUNtOWpMM2QwZEhscmVuRjNXbk50TjNkdGFIcFdXRFpuZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJGQldVUldVakJTUVZGSUwwSkdOSGRZU1ZwaFlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d6UWpWa1IyaDJZbWs0ZFZveWJEQmhTRlpwVEROa2RtTnRkRzFpUnprelkzazVlVnBYZUd4WldFNXNURzVzYUdKWGVFRmpiVlp0Q21ONU9XOWFWMFpyWTNrNWRGbFhiSFZOUkd0SFEybHpSMEZSVVVKbk56aDNRVkZGUlVzeWFEQmtTRUo2VDJrNGRtUkhPWEphVnpSMVdWZE9NR0ZYT1hVS1kzazFibUZZVW05a1Ywb3hZekpXZVZreU9YVmtSMVoxWkVNMWFtSXlNSGRHWjFsTFMzZFpRa0pCUjBSMmVrRkNRV2RSU1dNeVRtOWFWMUl4WWtkVmR3cE9aMWxMUzNkWlFrSkJSMFIyZWtGQ1FYZFJiMXBFUW1oTmVrWnBUVEpGTUZsdFdUQk9WRlpyVFdwcmQxbHRSbWxaYW1ONlRWZE9hRmxVVm1sYVYwVXhDazE2VFRCT1IxRXdXV3BCWTBKbmIzSkNaMFZGUVZsUEwwMUJSVVZDUVRWRVkyMVdhR1JIVldkVmJWWnpXbGRHZWxwVVFXMUNaMjl5UW1kRlJVRlpUeThLVFVGRlJrSkNhR3BoUjBad1ltMWtNVmxZU210TVYyeDBXVmRrYkdONU9YZGxXRkp2WWpJMGQwaFJXVXRMZDFsQ1FrRkhSSFo2UVVKQ1oxRlFZMjFXYlFwamVUbHZXbGRHYTJONU9YUlpWMngxVFVsSFMwSm5iM0pDWjBWRlFXUmFOVUZuVVVOQ1NIZEZaV2RDTkVGSVdVRXpWREIzWVhOaVNFVlVTbXBIVWpSakNtMVhZek5CY1VwTFdISnFaVkJMTXk5b05IQjVaME00Y0Rkdk5FRkJRVWRGVWxnNVRtVkJRVUZDUVUxQlVucENSa0ZwUlVGMVVrZEdLMGRGTmsxWWNsa0taa05EZUVFMU5DOVVVVzQwU3psaVVWSlpjRmR5U0ZoSFEwMXFPVFJ4VlVOSlIzWkJkR0ZhZVc1UVRIZExSbVJRZW5KMWJEQkxiMUpzZWxCVlR6SlZSd3BQVmxRelVqRm1Wekp3Y1U5TlFXOUhRME54UjFOTk5EbENRVTFFUVRKblFVMUhWVU5OVVVOaE1YQnFUMkpPT0VWTFRURnNVWFJ6YVRaYU9EbDFkbWQxQ2tkUFFtOWpMM0V5VG5KamJHTkdlbVZ1SzBscllscFViVUZCZWpabFFrcFBTRk5vZVdwM1dVTk5SbVpzY1c1d2JsUnplbmRGS3pGSloyZHlUSEUzVEVNS1RWYzRUVWhvVUVsT2VGVlNiWEI0VFRST2RpdDROMnN3VGtsR01IbzFWWE15SzFaU2VteFJkV2RuUFQwS0xTMHRMUzFGVGtRZ1EwVlNWRWxHU1VOQlZFVXRMUzB0TFFvPSJ9fX19",
          "integratedTime": 1667613302,
          "logIndex": 6531794,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/python/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/python",
      "githubWorkflowSha": "d0a31b3a4bf455d290babb731caa5bea53344d4b",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3398231657",
      "sha": "d0a31b3a4bf455d290babb731caa5bea53344d4b"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

