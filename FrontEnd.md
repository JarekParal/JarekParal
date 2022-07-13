# FrontEnd development tricks

## Testing

Run test:
```sh
npx jest modulation-map.c --watch
```

### Sergio test library
```ts
import { fake, Host, NgBench } from '@smazzoleni/testbed-extended';

    beforeEach(async () => {
        host = await NgBench.testComponent(ModulationMapComponent)
            .mockPipe('translate')
            .import(FormsModule)
            .mockProvider(LoadedLotService, {
                lot$: new Subject(),
                selectedMeasureResult$: new Subject(),
            })
            .mockComponents(NimoImageComponent)
            .createHost();
    });
```

Log HTML content of the module:
```ts
let host: Host<ModulationMapComponent>;

...

host.debug()
```
