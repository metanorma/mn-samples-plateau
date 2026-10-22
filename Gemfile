source "https://rubygems.org"

# metanorma core stack: git main
gem "metanorma-cli", "1.18.0.pre.alpha.1" #$(1)
gem "metanorma-core", "0.2.5.pre.alpha.1" #$(1)
gem "metanorma", "2.5.6.pre.alpha.1" #$(1)
gem "metanorma-standoc", "3.5.1.pre.alpha.1" #$(1)
gem "metanorma-document", "0.5.2.pre.alpha.1" #$(1)
gem "metanorma-utils", github: "metanorma/metanorma-utils", branch: "main"
gem "html2doc", git: "https://github.com/metanorma/html2doc", branch: "main"
gem "isodoc", "3.7.4.pre.alpha.1" #$(1)
gem "isodoc-i18n", "1.5.4.pre.alpha.1" #$(1)
gem "mn-requirements", git: "https://github.com/metanorma/mn-requirements", branch: "main"

# flavors: git main
gem "metanorma-plateau", "1.3.2.pre.alpha.1" #$(1)
gem "metanorma-iso", "3.5.1.pre.alpha.1" #$(1)
gem "metanorma-ieee", "1.7.1.pre.alpha.1" #$(1)
gem "metanorma-itu", "2.9.3.pre.alpha.1" #$(1)
gem "metanorma-iec", "2.9.1.pre.alpha.1" #$(1)
gem "metanorma-jis", "1.2.1.pre.alpha.1" #$(1)
# released shadow flavors (lib/relaton/render shipped in 1.x/2.x gems) crash
# boot under render 3.x (isodoc's compatibility require picks the shadow):
# ogc, iho, ietf, bipm still need git main until their shadow-free cuts land
gem "metanorma-ogc", "2.10.1.pre.alpha.1" #$(1)
gem "metanorma-iho", "1.4.1.pre.alpha.1" #$(1)
gem "metanorma-ietf", "3.7.12.pre.alpha.1" #$(1)
gem "metanorma-bipm", "2.9.1.pre.alpha.1" #$(1)

# lutaml family

# relaton / pubid line
gem "relaton", "~> 3.0.0.pre.alpha"
gem "relaton-cli", "~> 3.0.0.pre.alpha"
gem "relaton-render", "~> 3.0.0.pre.alpha"
gem "pubid", "~> 2.0.0.pre.alpha"

# corpus extras
gem "glossarist"
gem "lutaml-hal"
gem "lutaml-lml"
gem "lutaml-store"
gem "parsanol"
gem "canon"
gem "yeptris"
gem "tzinfo-data"
gem "word-to-markdown"

# tooling
gem "debug"
gem "ffi"
gem "sassc-embedded"

# transitive pre-stack gems: root pins make prereleases admissible for
# their gemspec constraints
gem "metanorma-taste", "1.1.3.pre.alpha.1"
gem "metanorma-plugin-datastruct", "0.3.12.pre.alpha.1"
