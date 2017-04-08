# DK Nonces

## Introduction

Dinamiko Nonces allows working with WordPress Nonces in an easy way.

## Table of Contents

* [Installation](#installation)
* [Usage](#usage)
* [Run the tests](#run-the-tests)

## Installation

Install with [Composer](https://getcomposer.org):

```sh
$ composer require dinamiko/nonces
```

## Usage

Create a nonce:

```php
$nonce = new Dinamiko\Nonces\Nonce( 'my-action' );
```

Create a nonce field:

```php
$nonce = new Dinamiko\Nonces\Nonce( 'my-action' );
$field = $nonce->create_field();
```

Create a nonce URL:

```php
$nonce = new Dinamiko\Nonces\Nonce( 'my-action' );
$url = $nonce->create_url( 'http://example.com' );
```

Verify a nonce:

```php
$nonce = new Dinamiko\Nonces\Nonce( 'my-action' );
$is_valid = $nonce->is_valid( $_POST['foo'] );
```

## Run the tests

```sh
$ cd vendor/dinamiko/nonces
$ composer install
$ vendor/bin/phpunit
```
