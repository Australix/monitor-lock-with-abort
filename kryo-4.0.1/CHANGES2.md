* Fixed #248. There was a bug in the buffer resizing code. ([23830f6](https://github.com/EsotericSoftware/kryo/commit/23830f64cffd7ee7844fc582ef2b68023aeab908))
* end() for deflater and inflater. ([a306471](https://github.com/EsotericSoftware/kryo/commit/a3064716bb47c64e55b0048a6f5dac15dd67aabe))
* Fixed DeflateSerializer. ([86aecf1](https://github.com/EsotericSoftware/kryo/commit/86aecf10b522bb99e126e2c89cfab33ad00d03d0))
* BigIntegerSerializer, BigDecimalSerializer, TreeMapSerializer and TreeSetSerializer optimizations and enhacements:   - Proper handle of subclasses (Fix #166)   - Small optimizations for common BigDecimal and BigInteger constants (Fix #238)   - Unit test to avoid regression of PermGen leaks (ensure fix of #170 contributed by #173) ([2d6204d](https://github.com/EsotericSoftware/kryo/commit/2d6204dc5a04c10689a413d5365a607bdd1edab9))
* Remove unnecesary code ([8efb79c](https://github.com/EsotericSoftware/kryo/commit/8efb79c163b7ad539cb3099782e218b5bbe272f6))
* Override writeChar and readChar methods to use unsafe: writeChar now performs about 125% faster and readChar 10% faster than overriden safe versions. ([45f510d](https://github.com/EsotericSoftware/kryo/commit/45f510de2dc07a65cf3807f28f6a9f9aa1749aca))
* Small optimization ([19d88db](https://github.com/EsotericSoftware/kryo/commit/19d88db264a912fbc2ed33149a4398b91cc89202))
* Fix a NPE ([004cc5c](https://github.com/EsotericSoftware/kryo/commit/004cc5cd2a6c2ecc2c839f34ab5ce4951ca32700))
* DateSerializer and LocaleSerializer enhacements and tests ([ac4ebef](https://github.com/EsotericSoftware/kryo/commit/ac4ebef070f82a419263c97d18146c35d9e0cde7))
* DateSerializer and LocaleSerializer enhacements and tests ([9e63c65](https://github.com/EsotericSoftware/kryo/commit/9e63c65c51937c1a6d95ec2f7a972112fa37ee5b))
*  ([442f630](https://github.com/EsotericSoftware/kryo/commit/442f630196aba89f800282407dc2064d0874d201))
* Unit tests for DateSerializer and LocaleSerializer ([2f403c7](https://github.com/EsotericSoftware/kryo/commit/2f403c7b26fa056cd1bd807d3c330d5731e61193))
* (*) Enhacements to DateSerializer: use identity comparison (*) Enhacements to LocaleSerializer:   - removed copy method, as Locale isImmutable   - reordered and enhacements to the Locale constants search inside the create method   - optimized write method: use writeAscii for language and country fields (not for variant) ([213a767](https://github.com/EsotericSoftware/kryo/commit/213a767a87a0e067d38b25bdd3c2f33e0ca0d31e))
* Fix serializers reference ([9db3ef4](https://github.com/EsotericSoftware/kryo/commit/9db3ef4b63a65bebfde2929179e5dc0176ecc6f2))
* Change KryoPool to interface + Builder, make SoftReferences optional. ([38c6815](https://github.com/EsotericSoftware/kryo/commit/38c681594cb48876f88b83cda731752d4b387a1f))
* Set StdInstantiatorStrategy as default fallback instantiator strategy. ([0a43a64](https://github.com/EsotericSoftware/kryo/commit/0a43a642f4fe77d7cf6d7ee22b44d4e2bac568e2))
* Fix #223. setTotal should take long as a parameter. ([ffe6931](https://github.com/EsotericSoftware/kryo/commit/ffe6931b559c1579f44936f13e73a9f71640a96b))
* Bump version to 2.25.0-SNAPSHOT ([ca153ba](https://github.com/EsotericSoftware/kryo/commit/ca153ba7deca816f9b95405e6cf956da56f2e464))
* Change groupId to com.esotericsoftware. ([d8e519a](https://github.com/EsotericSoftware/kryo/commit/d8e519a65dc16d06ec37e25dfc2cc11a7332ee2f))
* Fix shaded pom to use the correct reflectasm groupId ([4259143](https://github.com/EsotericSoftware/kryo/commit/425914333db7271536dcb6f0f34c6bac8bf5f3e6))
* Add simple, queue based kryo pool. ([05fed9c](https://github.com/EsotericSoftware/kryo/commit/05fed9cfe0a775afa38c49c34822c10193d7b67a))
* Change default artifact *not* to shade reflectasm, use OSGi'ed reflectasm 1.3.0 ([e1e3b0b](https://github.com/EsotericSoftware/kryo/commit/e1e3b0b18684961bd0b97665a4e662ec64b8c1e5))
* Update minlog to 1.3.0 which is now OSGi'ed ([de5d2a3](https://github.com/EsotericSoftware/kryo/commit/de5d2a3209c3122031f130e82f0267e7229ae731))
* Add automated compatibility check (with previous version) ([f85d6c9](https://github.com/EsotericSoftware/kryo/commit/f85d6c98a371b4c25f1fcc5e753855e5371e279d))
* Fixed #227 ([96f7225](https://github.com/EsotericSoftware/kryo/commit/96f7225694322e27268dd698fefdffff5f4cfb6c))
* Exception -> Throwable ([1f0ba1b](https://github.com/EsotericSoftware/kryo/commit/1f0ba1b94c83cf26fc6ce108641d32c2e3c171c3))
* Update README.md ([e000a0a](https://github.com/EsotericSoftware/kryo/commit/e000a0a2d1414107321742334a5001bdd21eba39))
* Recover from exceptions in Util.string() ([2d15fc2](https://github.com/EsotericSoftware/kryo/commit/2d15fc2652ee777ba153409be0b258b30fc8a6ff))
* Revert "Fix #223. setTotal should take long as a parameter." ([4cd880b](https://github.com/EsotericSoftware/kryo/commit/4cd880bcefa532f9660a0009ff1059bad4b5e509))
* Fix #223. setTotal should take long as a parameter. ([62ea11b](https://github.com/EsotericSoftware/kryo/commit/62ea11b0c684f8ee715e5e31a4195a1c28b47a2a))
* Properly handle removal of transient fields. Till now it was not possible to remove them. ([faca949](https://github.com/EsotericSoftware/kryo/commit/faca94981c41aa9bd92a8a7f81b073d6b85ba0c4))
* issue 218 ([3bac35c](https://github.com/EsotericSoftware/kryo/commit/3bac35c8f28216295b391372e89a6cbf61b943a0))
* Improve description of java serialization, unsafe IO and instantiation. ([7fa98c6](https://github.com/EsotericSoftware/kryo/commit/7fa98c64d30ca9c8b22f647da487c4c8cacbd6cb))
* Add support for serialization of Java8 closures (see #215). ([0b733dd](https://github.com/EsotericSoftware/kryo/commit/0b733ddad02e51b08e85a28fd960790ff4e69e8e))
* Restructure README ([2881130](https://github.com/EsotericSoftware/kryo/commit/28811302f19eaebf3f3ec77edee18c51387bca41))
* Refer to changelog ([f5ac469](https://github.com/EsotericSoftware/kryo/commit/f5ac46954f43c4c91731a039e7be2a7d20124496))
* Update README.txt with information about current release, field annotations and using of Kryo without Maven. ([f780073](https://github.com/EsotericSoftware/kryo/commit/f780073a7f198ff8ffa3f36a0eba49c1282f8b51))
* Update project.yaml to reflect the new development version ([08b8d7c](https://github.com/EsotericSoftware/kryo/commit/08b8d7caab5e6b9333e5194abb4dc25b6e40c78c))
* Reformat CHANGES to include links to issues ([01aa150](https://github.com/EsotericSoftware/kryo/commit/01aa150f6b54fd537e6e2e73d419ddb87cdba55d))
* Update README for the 2.24.0 release ([439a95d](https://github.com/EsotericSoftware/kryo/commit/439a95d1986d453e963136e221e691f8e9c52a50))
* Update CHANGES for 2.24.0 release, add compat reports ([94ecccb](https://github.com/EsotericSoftware/kryo/commit/94ecccb3170623b2cb38f22776a70a304febfd65))
* [maven-release-plugin] prepare for next development iteration ([0cbea0a](https://github.com/EsotericSoftware/kryo/commit/0cbea0a36e6a4183ab1b7b4c1a93eb4a0f81b6e5))