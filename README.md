# react-kb-form

Form validation hook library for enterprise scale react applications

## Installation

Use the package manager [npm](https://www.npmjs.com/package/react-kb-form) to install react-kb-form.

```bash
npm i react-kb-form
```

## Simple Usage

```javascript
import { useKBform } from "react-kb-form";

const {
  _register,
  _handleSubmit,
  _envMode,
  _reset,
  watchState,
  formState,
  errorState,
  formStatus,
} = useKBform();

<form ref={_register} _formname="form" onSubmit={_handleSubmit}>
  <input name="surname" _required="true" />
  {errorState.surname}

  <button type="submit">submit</button>
</form>;

useEffect(() => {
  if (formState) {
    console.log(formState.form);
  }
}, [formState]);
```

# Available Props

```javascript

    _required: string;
    _number: string;
    _min: string;
    _max: string;
    _password: string;
    _passwordrepeat: string;
    _strongpassword: string;
    _minlength: string;
    _maxlength: string;
    _length: string;
    _email: string;
    _amount: string;
    _pan: string;
    _panbasic: string;
    _pin: string;
    _formname: string;
    _customrege?: string;
    _resetbtn: string;
    _ignore: string;
    _phone: string;

```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
