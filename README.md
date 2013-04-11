# JOSEPh

PHP JOSE Implementation

# Example

## JWT

### Encoding

    $jwt = new JOSEPh_JWT(array(
        'foo' => 'bar'
    ));
    $jwt->toString();

### Decoding

    $jwt_string = 'eyJ...';
    $jwt = JOSEPh_JWT::decode($jwt_string);

## JWS

### Signing

    $jwt = new JOSEPh_JWT(array(
        'foo' => 'bar'
    ));
    $jws = $jwt->sign($private_key, 'RS256');

### Verification

    $jwt_string = 'eyJ...';
    $jwt = JOSEPh_JWT::decode($jwt_string);
    $jwt->verify($public_key);

## JWE

### Encryption

not supported yet

### Decryption

    $jwt_string = 'eyJ...';
    $jwt = JOSEPh_JWT::decode($jwt_string);
    $jwt->decrypt($private_key);

# Copyright

Copyright © 2011 GREE Inc. See LICENSE for details.