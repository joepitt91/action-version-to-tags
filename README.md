<!--
SPDX-FileCopyrightText: 2025 Joe Pitt

SPDX-License-Identifier: GPL-3.0-only
-->
# GitHub Action - Convert Version to Tags

Convert semantic version number to container image tags.

## Inputs

| Input | Description | Required | Default |
|-------|-------------|----------|---------|
| version | The semantic version number to convert. | Yes |  |

## Outputs

| Output | Description | Example |
|--------|-------------|---------|
| major_tag | The tag for major version. | 3 |
| minor_tag | The tag for minor version. | 3.2 |
| patch_tag | The tag for patch version. | 3.2.87 |

## Example

```yaml
      - name: Convert Version to Tags
        id: version
        uses: joepitt91/action-version-to-tags@v1
        with:
          version: ${{ steps.version.outputs.version }}
```
