source "https://rubygems.org"

gem "metanorma-cli" #, git: "https://github.com/metanorma/metanorma-cli"
# metanorma 2.5.5 needs Metanorma::Core::Flavors; rubygems' metanorma-core 0.2.3 lacks it
gem "metanorma-core", git: "https://github.com/metanorma/metanorma-core", branch: "main"
gem "ffi"

# For development only
gem "html2doc", git: "https://github.com/metanorma/html2doc", branch: "main"
gem "isodoc-i18n", git: "https://github.com/metanorma/isodoc-i18n", branch: "main"
gem "isodoc", git: "https://github.com/metanorma/isodoc", branch: "main"
gem "metanorma-standoc", git: "https://github.com/metanorma/metanorma-standoc", branch: "main"
# standoc main references Metanorma::Document::Components constants; the
# metanorma-document gem must be in the bundle for them to resolve
gem "metanorma-document", git: "https://github.com/metanorma/metanorma-document", branch: "main"
# metanorma-document main requires metanorma/mko; only metanorma main provides it
gem "metanorma", git: "https://github.com/metanorma/metanorma", branch: "main"
# flavors referenced by the plateau handbook corpus
gem "metanorma-ieee"
gem "metanorma-itu"
gem "metanorma-iec"
# metanorma-ieee/itu/iec require these but their gemspecs omit them
gem "pubid-ieee"
gem "pubid-itu"
gem "pubid-iec"
gem "metanorma-iso", git: "https://github.com/metanorma/metanorma-iso", branch: "main"
gem "metanorma-jis", git: "https://github.com/metanorma/metanorma-jis", branch: "main"
gem "metanorma-plateau", git: "https://github.com/metanorma/metanorma-plateau", branch: "main"
gem "metanorma-utils", git: "https://github.com/metanorma/metanorma-utils", branch: "main"
gem "mn-requirements", git: "https://github.com/metanorma/mn-requirements", branch: "main"
# git-main relaton-render removed Relaton::Render::General, breaking isodoc;
# released 1.3.0 matches isodoc and the harness bundles
# gem "relaton-render", git: "https://github.com/relaton/relaton-render", branch: "main"
gem "debug"
gem "sassc-embedded"
