[![Build Status](https://travis-ci.org/cfn-modules/alb-listener.svg?branch=master)](https://travis-ci.org/cfn-modules/alb-listener)
[![NPM version](https://img.shields.io/npm/v/@cfn-modules/alb-listener.svg)](https://www.npmjs.com/package/@cfn-modules/alb-listener)

# cfn-modules: ALB listener

ALB listener.

## Install

> Install [Node.js and npm](https://nodejs.org/) first!

```
npm i @cfn-modules/alb-listener
```

## Usage

```
---
AWSTemplateFormatVersion: '2010-09-09'
Description: 'cfn-modules example'
Resources:
  AlbListener:
    Type: 'AWS::CloudFormation::Stack'
    Properties:
      Parameters:
        AlbModule: !GetAtt 'Alb.Outputs.StackName' # required
        Port: '80' # optional
        CertificateArn: '' # optional
      TemplateURL: './node_modules/@cfn-modules/alb-listener/module.yml'
```

## Parameters

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Default</th>
      <th>Required?</th>
      <th>Allowed values</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>AlbModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/alb">alb module</a></td>
      <td></td>
      <td>yes</td>
      <td></td>
    </tr>
    <tr>
      <td>Port</td>
      <td>The port on which the listener listens for requests</td>
      <td>80</td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>CertificateArn</td>
      <td>Amazon Resource Name (ARN) of the certificate to associate with the listener</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
  </tbody>
</table>
