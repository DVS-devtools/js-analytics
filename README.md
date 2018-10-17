# js-analytics

[![Build Status](https://travis-ci.com/docomodigital/js-analytics.svg?branch=master)](https://travis-ci.com/docomodigital/js-analytics)
[![Coverage Status](https://coveralls.io/repos/github/docomodigital/js-analytics/badge.svg)](https://coveralls.io/github/docomodigital/js-analytics)
[![npm version](https://badge.fury.io/js/%40docomodigital%2Fjs-analytics.svg)](https://badge.fury.io/js/%40docomodigital%2Fjs-analytics)
[![Greenkeeper badge](https://badges.greenkeeper.io/docomodigital/js-analytics.svg)](https://greenkeeper.io/)

js-analytics is a interface for Google Analytics to tracking events, pageviews and custom dimensions

## Usage
```javascript
import JsAnalytics from '@docomogital/js-analytics'
// init JsAnalytics and set 'User' custom dim to slot #3 and 'Valuable' to slot #4
JsAnalytics.init({
	enabled: true,
	logger: console,
	dimensions: {
		User: 3,
		Valuable: 4
	}
});

// set 'User' custom dim, without re-specify the slot
JsAnalytics.setDimension({
	User: 'logged'
});

// track pageview
JsAnalytics.trackPage({
	page: '/home',
	title: 'Home Page',
	dimensions: {
		Valuable: false
	}
});

// track event
JsAnalytics.trackEvent({
	category: 'Social',
	action: 'Click',
	label: 'Facebook',
	value: 3,
	dimensions: {
		Valuable: true
	}
});
```

## Installation

### NPM
```bash
npm install --save @docomogital/js-analytics
```

## Documentation

To read documentation, go to:

[http://docomodigital.github.io/js-analytics/latest](http://docomodigital.github.io/js-analytics/latest)
