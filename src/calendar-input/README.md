```jsx
<div>
    {['s', 'm', 'l', 'xl'].map(size => (
        <div className='row' key={ size }>
            <CalendarInput
                size={ size }
                defaultValue='01.02.2016'
            />
        </div>
    ))}
</div>
```

```jsx
<div>
    {['s', 'm', 'l', 'xl'].map(size => (
        <div className='row' key={ size }>
            <CalendarInput size={ size } defaultValue='41.12.2031' error='Такой даты не существует' />
        </div>
    ))}
</div>
```

```jsx
const formatDate = require('date-fns/format');

<div>
    {['s', 'm', 'l', 'xl'].map(size => (
        <div className='row' key={ size }>
            <CalendarInput size={ size } placeholder={ formatDate(new Date(), 'DD.MM.YYYY') } width='available' />
        </div>
    ))}
</div>
```

Без фолбэка на нативный контрол на мобильном устройстве
```
<div>
    <CalendarInput
        size='m'
        defaultValue='01.10.2017'
        mobileMode='popup'
    />
</div>
```
