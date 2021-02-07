# Index
* [howto-archive](/_user_manual_/howto_archive.md)
* **howto-react**
* [howto-script](/_user_manual_/howto_script.md)
* [Docker](/_user_manual_/howto_archive-docker.md)

# react-howto
[![NPM](https://img.shields.io/npm/v/@yazilim-vip/howto-react.svg)](https://www.npmjs.com/package/@yazilim-vip/howto-react) 
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-typescript-brightgreen.svg)](https://standardjs.com) 
[![License](https://img.shields.io/github/license/yazilim-vip/howto-react)](https://github.com/yazilim-vip/howto-react/blob/main/LICENSE)
[![Stars](https://img.shields.io/github/stars/yazilim-vip/howto-react)](https://github.com/yazilim-vip/howto-react)


## Install
Install with yarn
```yarn
npm install --save @yazilim-vip/react-howto
```
Install with npm
```bash
npm install --save @yazilim-vip/react-howto
```

## Usage

```tsx
import  from 'react'

import { HowToContainer } from '@yazilim-vip/react-howto'

export const  Example = () => (
    <HowToContainer
        rootCategory={howToData}
        requestedPath={requestedPath}
        events={{
            itemSelectEventHandler: (type, link) => {
                // handle item select event 
            }
        }}
    />
)
```

### Examples
* [Yazilim VIP HowTo Archive:](https://howto.yazilim.vip) 

## License

MIT © [Yazilim VIP](https://github.com/yazilim-vip/react-howto)
