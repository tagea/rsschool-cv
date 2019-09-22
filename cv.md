# Resume

## Pesonal info

My name is **Vasilyeva Yulya**.

| source   | value                                                         |
| :------- | :------------------------------------------------------------ |
| phone    | [+375296858506](tel:+375296858506)                            |
| email    | [yulyavasilyeva@gmail.com](mailto:yulyavasilyeva@gmail.com)   |
| site     | [yulyavasilyeva.ru](https://yulyavasilyeva.ru)                |
| skype    | live:114385cb8ed3ac93                                         |
| telegram | tagea23                                                       |
| linkedin | [yulyavasilyeva](https://www.linkedin.com/in/yulyavasilyeva/) |

In the short term, one of my goals is to continue developing my **frontend skills**. I want to improve knowledge in UX and create the user-accessible interface. Over the past two years, I've gained knowledge of frontend development. I don't have enough skills in programming that why some of the tasks up a lot of time. Every day I try to know something new in the developing environment. I like to create art and fashion photos, improve in computer graphics and animation.

## Skills
- HTML (HTML5)
- CSS (CSS3)
- Less, SASS
- SVG
- Bootstrap, Material UI, Foundation
- JavaScript (ES6)
- JQuery
- React
- Styled
- WebPack, Gulp
- Git
- Jest
- Adobe After Effects, Adobe Photoshop
- Autodesk 3ds Max, Autodesk Maya


### Part of the React project
```
import React, { useState, useEffect } from 'react';
import { Redirect } from 'react-router-dom';
import { connect } from 'react-redux';
import PropTypes from 'prop-types';

import { Auth } from '../components/Auth';
import { signInAction, stayInAction } from '../services/auth/actions';

import { ROUTE_PATHS } from '../utils/paths';

const AuthContainer = (props) => {
  const [form, changeInput] = useState({ username: '', password: '' });
  const { authenticated, error } = props;

  useEffect(() => {
    props.stayIn();
  });

  const handleChangeInput = (ev) => {
    changeInput({
      ...form,
      [ev.target.name]: ev.target.value
    });
  };

  const handleSubmit = () => {
    props.signIn(form.username, form.password);
  };

  const pressEnter = (ev) => {
    if (ev.key === 'Enter') {
      handleSubmit();
    }
  };

  if (authenticated) {
    return <Redirect to={ROUTE_PATHS.root} />;
  }
  return (
    <Auth
      error={error}
      value={form}
      handleChangeInput={handleChangeInput}
      pressEnter={pressEnter}
      handleSubmit={handleSubmit}
    />
  );
};

AuthContainer.propTypes = {
  error: PropTypes.bool,
  authenticated: PropTypes.bool,
  stayIn: PropTypes.func.isRequired,
  signIn: PropTypes.func.isRequired
};

AuthContainer.defaultProps = {
  error: false,
  authenticated: false
};


const mapStateToProps = (state) => ({
  authenticated: state.auth.authenticated,
  error: state.auth.error
});

const mapDispatchToProps = (dispatch) => ({
  stayIn: () => dispatch(stayInAction()),
  signIn: (username, password) => dispatch(signInAction(username, password))
});

export default connect(
  mapStateToProps,
  mapDispatchToProps
)(AuthContainer);
```

## Experience

- since July 2019 - working in the web-studio Webcat as Frontend developer (landing page, HTML, CSS jQuery, PHP)
- since February 2019 - internship in the opensource project ["Manicure"](http://github.com/tagea/manicure-web-support) (SPA, Redux, Jest/Enzyme, REST API, Material UI + styled-components, ESLint, Webpack)
- from December 2018 to February 2019 -  internship in the project [Checklist](http://github.com/gtd-checklist/checklist-web) (SPA, Redux, Material UI + styled-components, REST API, React Route + HashRouter, ESLint, Webpack)
- personal project ["Task Manager"](https://yulyavasilyeva.ru/task-manager) (SPA, Redux, Ant Design, authorization, get data from REST API, ESLint, Webpack)
- projects from courses 
  - ["Waxom"](http://tagea.github.io/Waxom-landing/) (HTML5, Bootstrap Grid)
  - ["Go RUN"](https://tagea.github.io/goRUN/) (css animation, css transform, gradient, SVG, clip-path)
  - ["Interior Design"](http://tagea.github.io/Studio-interior-Bootstrap/) (adaptive, WOW scroll, Swiper)
  - ["Library"](https://github.com/tagea/Cinema-List) (JS classes, functions, DOM)


## Education

- European Humanities University (*2004 - 2005*), faculty of information technology, specialty: Web-design and computer graphic
- Institute of Modern Knowledge (*2005 - 2007*), faculty of economic, specialty: Web-design and computer graphic
- Belarusian State University (*2007 - 2008*), faculty of liberal education, specialty: Web-design and computer graphic


## English

Streamline english Language Course: 2013 - 2014 (A1)

School of English Belhard, Spoken English Language Course Pre-Intermediate Level: 2018 (B1)