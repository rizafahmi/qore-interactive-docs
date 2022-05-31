---
title: Quickstart dengan React
date: Last Modified
permalink: /react/
eleventyNavigation:
  key: react
  order: 2
  title: React
  parent: quickstart
---

# Menyiapkan Qore

Sebelum membuat karya dengan React, siapkan terlebih dahulu aplikasi di sisi Qore.

## Membuat Karya Baru

1. Menuju ke https://console.qore.sh/
2. Tekan tombol "New Project"
3. Masukkan informasi yang dibutuhkan

## Menyiapkan Table dan View

Pilih karya yang tadi dibuat dan akan menuju ke halaman detil karya.

![project](/content/images/59eba633243b79985dc1c60001c73ab3288d288ba2d5f0afd854c5158f6d127366d77b68cdcb12131f23dbc9e8940cd24c1ac86cbcf4e05c6752687091dfa71641dbb45ae58fb466be818bf6e191ccb466934c0aceab186eb19f76ede892a36ddbb70779.jpeg)

[TODO: Lanjutin nanti]

# Membuat Karya dengan React

Mari membuat karya React dari awal dengan bantuan [create react app](https://create-react-app.dev/docs/getting-started/) dan beri nama qore-react.

```shell
npx create-react-app qore-react
cd qore-react
```

## Instalasi Pustaka Qore

Lakukan instalasi berbagai pustaka Qore yang dibutuhkan.

```shell
npm install @feedloop/qore-client
npm install @feedloop/qore-react
npm install --save-dev @feedloop/qore-cli
```

Login ke Qore dari _command-line_ dengan qore-cli.

```shell
npx qore login
```

Kemudian buat koneksi antara karya Qore dengan karya React. Pilih organisasi dan karya Qore yang sesuai.

```shell
npx qore set-project
```

Jalankan codegen untuk mendapatkan file konfigurasi yang tepat. Agar berada di folder `src/` seperti kode React lainnya, tambahkan tanda `---path`

```shell
npx qore codegen --path src
```

## Mempersiapkan Qore untuk Komponen React

Buat sebuah file di `src/qoreClient.js` untuk menggunakan Qore di komponen React.

### `src/qoreClient.js`

```javascript
import { QoreClient } from '@feedloop/qore-client';
import createQoreContext from '@feedloop/qore-react';
import config from './qore.config.json';
import schema from './qore.schema.json';

const client = new QoreClient(config);
client.init(schema);

const qoreContext = createQoreContext(client);
export default qoreContext;
```

Lalu bungkus komponen utama dengan qoreClient.

### `src/index.js`

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';

import qoreContext from './qoreContext.js';

ReactDOM.render(
  <React.StrictMode>
    <qoreContext.context.Provider
      value={{
        client: qoreContext.client,
      }}
    >
      <App />
    </qoreContext.context.Provider>
  </React.StrictMode>,
  document.getElementById('root')
);
```

## Seluruh Kode

<div class="glitch-embed-wrap" style="height: 420px; width: 100%;">
  <iframe
    src="https://glitch.com/embed/#!/embed/qore-cra-glitch?path=src/qoreContext.js&previewSize=0"
    title="qore-cra-glitch on Glitch"
    allow="geolocation; microphone; camera; midi; vr; encrypted-media"
    style="height: 100%; width: 100%; border: 0;">
  </iframe>
</div>
