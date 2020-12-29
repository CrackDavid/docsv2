+++
title = "FAQ"
date = 2020-12-29T19:33:11+10:00
weight = 1
+++

## Technical Questions

### Why did you not use Go 1.16's asset embedding?

The new embed feature in Go is great, but it is not 100% aligned with our use case. The majority of assets we need to embed are assets for the front end. These assets are entirely managed in C, and whilst we could copy them over into C managed code, it is inefficient to do so. Version 1 of Wails does this and there's a significant startup penalty. In v2, we actually create C files for the embedded assets so they can be used directly by the frontend in their raw form.
