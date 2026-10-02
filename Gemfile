source "https://rubygems.org"

# Git gems below are pinned to the exact revisions validated by the green
# docker workflow run 36709538685 (2026-09-30, main @ ccd4bc2). Together with
# the committed Gemfile.lock this keeps CI reproducible — floating
# `branch: "main"` deps previously broke the deployment when upstream changed.

gem "metanorma-cli" #, git: "https://github.com/metanorma/metanorma-cli"
# metanorma 2.5.5 needs Metanorma::Core::Flavors; rubygems' metanorma-core 0.2.3 lacks it
gem "metanorma-core", git: "https://github.com/metanorma/metanorma-core", ref: "b5312cea1ba34b872311b2a3c39b0b5a081db463"
gem "ffi"

# For development only
gem "html2doc", git: "https://github.com/metanorma/html2doc", ref: "4b54dfaf9c96ec6535fed2847bed1c37aa64c49b"
gem "isodoc-i18n", git: "https://github.com/metanorma/isodoc-i18n", ref: "2f8c4e53d1f14778a08dbd43a7a255100aacc329"
gem "isodoc", git: "https://github.com/metanorma/isodoc", ref: "d75b68711b01b548aad85cf378bee532d02cd945"
gem "metanorma-standoc", git: "https://github.com/metanorma/metanorma-standoc", ref: "6b67105dec22e7d9d6870274872ba1d651a5c325"
# standoc main references Metanorma::Document::Components constants; the
# metanorma-document gem must be in the bundle for them to resolve
gem "metanorma-document", git: "https://github.com/metanorma/metanorma-document", ref: "d676560e801ccc69fae5a2b50bc79f15794c668a"
# metanorma-document main requires metanorma/mko; only metanorma main provides it
gem "metanorma", git: "https://github.com/metanorma/metanorma", ref: "c84982c98596ccd88ff71d0e54b7d04d8ad396a6"
# flavors referenced by the plateau handbook corpus
gem "metanorma-ieee"
gem "metanorma-itu"
gem "metanorma-iec"
# metanorma-ieee/itu/iec require these but their gemspecs omit them
gem "pubid-ieee"
gem "pubid-itu"
gem "pubid-iec"
gem "metanorma-iso", git: "https://github.com/metanorma/metanorma-iso", ref: "9b262b719d50f08c3e39bb316c60b4902d216375"
gem "metanorma-jis", git: "https://github.com/metanorma/metanorma-jis", ref: "d4f18b93d68b96b2a32b69b35ba95a4594106a30"
gem "metanorma-plateau", git: "https://github.com/metanorma/metanorma-plateau", ref: "6224318a92cd6b3f623455d643dbb418703e0ed0"
gem "metanorma-utils", git: "https://github.com/metanorma/metanorma-utils", ref: "5fda52af4a09cd3492911beb192e71879659491f"
gem "mn-requirements", git: "https://github.com/metanorma/mn-requirements", ref: "27f8a4b22b366dafa11323a4d827ce5ae9daed0d"
# git-main relaton-render removed Relaton::Render::General, breaking isodoc;
# released 1.3.0 matches isodoc and the harness bundles
# gem "relaton-render", git: "https://github.com/relaton/relaton-render", branch: "main"
gem "debug"
gem "sassc-embedded"

# Exact versions from the green run — later releases broke the build
gem "relaton", "= 3.0.0.pre.alpha.4"
gem "relaton-cli", "= 3.0.0.pre.alpha.4"
gem "lutaml-model", "= 0.8.87"
gem "moxml", "= 0.5.96"
gem "leptris", "= 1.9.277.0"
gem "yeptris", "= 0.6.26.2"
gem "canon", "= 0.3.76"
gem "ea", "= 0.6.12"
gem "glossarist", "= 2.14.0"
gem "lutaml-hal", "= 0.2.5"
gem "lutaml-lml", "= 0.1.5"
gem "lutaml-store", "= 0.2.4"
gem "parsanol", "= 1.3.57"
gem "tzinfo-data", "= 1.2026.4"
gem "word-to-markdown", "= 1.2.0"
