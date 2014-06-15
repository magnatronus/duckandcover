DuckAndCover
============

This is an example app that uses the alloy.jmk file to auto generate JSDuck documentation, inspired by an article by Ronald Treur on TiDev (http://www.tidev.io/2014/05/14/duckumentation/)

## Prerequisites

JSDuck should be installed

>gem install jsduck

then the only additional module that I used was xmldoc which can be installed using

>npm install xmldoc -g

This is used so that the tiapp.xml file can be decoded and the params within it used in generating the documentation. So if you don’t want to extract the tiapp.xml data you can leave this bit out (and comment or remove the associated code)

## What It Does
Using the hooks in the provided alloy.jmk file it automatically documents your Titanium project using JSDuck to a directory called appdocs in the root of your project. 
This process is run each time you compile you app when it runs the alloy.jmk file.

The only actual file required for a Titanium project is the alloy.jmk file itself, any other required files such as the jsduck.json config file, are auto generated. Just make a copy of alloy.jmk and add it to one of your existing projects. And, if you already have a jmk file then just append the relevent code.

When it runs it will create/update the documentation for your project (providing you have used the JSDuck tags within it).

## License

Licensed under the Apache License, Version 2.0 (the "License"). You may obtain a copy of the License from

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.