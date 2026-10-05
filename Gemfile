source "https://rubygems.org"

gem "metanorma-cli", git: "https://github.com/metanorma/metanorma-cli", branch: "main" # fleet pins for the 1.3-era flavors
# metanorma 2.5.5 needs Metanorma::Core::Flavors; rubygems' metanorma-core 0.2.3 lacks it
gem "metanorma-core", git: "https://github.com/metanorma/metanorma-core", branch: "main"
gem "ffi"

# For development only
gem "html2doc", git: "https://github.com/metanorma/html2doc", branch: "main"
gem "isodoc-i18n", git: "https://github.com/metanorma/isodoc-i18n", branch: "main"
gem "isodoc", git: "https://github.com/metanorma/isodoc", branch: "main"
gem "metanorma-standoc", github: "metanorma/metanorma-standoc", branch: "perf/cleanup-gc-budget" # standoc#1269: cleanup GC budget + in-place insert_xml_cr
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
gem "metanorma-iso", git: "https://github.com/metanorma/metanorma-iso", branch: "main"
gem "metanorma-jis", git: "https://github.com/metanorma/metanorma-jis", branch: "fix/restore-1-2-numbering" # PR 523: pubid-2 line relax
gem "metanorma-plateau", git: "https://github.com/metanorma/metanorma-plateau", branch: "main"
gem "metanorma-utils", git: "https://github.com/metanorma/metanorma-utils", branch: "perf/asciidoctor-table-buffer" # utils#55: GcBudget + in-place table cell buffer (asciidoctor quadratic)
gem "mn-requirements", git: "https://github.com/metanorma/mn-requirements", branch: "main"
# git-main relaton-render removed Relaton::Render::General, breaking isodoc;
# released 1.3.0 matches isodoc and the harness bundles
# gem "relaton-render", git: "https://github.com/relaton/relaton-render", branch: "main"
gem "debug"
gem "sassc-embedded"

# hyperperformance line: git-main for the whole lutaml family
gem "lutaml-model", github: "lutaml/lutaml-model", branch: "perf/hash-access-allocs" # lutaml-model#916: fetch_str_or_sym string births
gem "moxml", github: "lutaml/moxml", branch: "perf/node-set-intersection" # moxml#324: NodeSet set-ops + mutator adoption; byte-parity-validated here. wrapper-read-memos (#321 line) stacks on main separately
gem "leptris", "1.9.304" # v1.9.304: leptris#1528 fixed (cross-document splice adoption); #1528 was the sectioned-cleanup segfault
gem "ea", github: "lutaml/ea", branch: "perf/xmi-slicer" # ea#86: whole/partial loading (Ea::Xmi.load); flip to main on merge
gem "xmi", github: "lutaml/xmi", branch: "main"
gem "metanorma-plugin-lutaml", github: "metanorma/metanorma-plugin-lutaml", branch: "perf/xmi-slices" # plugin#311: partial load via Ea::Xmi.load_graph (lutaml-ea-xmi-load: partial); flip to main on merge

# asciidoctor (2.0.x) rebuilds the whole cell buffer String on every appended
# table line (O(N^2) per multi-line cell): the klass tables render a 57k-line
# cell (414KB) that allocates ~10GB of transients and OOMs 8GB builds.
# asciidoctor is third-party: the fix is carried inside metanorma-utils
# (utils#55, self-disarming when asciidoctor ships it) - no fork, no filing.

# monogems: relaton + pubid at git main (metanorma gems already depend on these
# names; released rubygems snapshots lag the monogem APIs)
# relaton main's new cache keys (relaton#240) miss the repo's local
# ref cache and storm the v2 indexes (multi-GB, OOMs 14GB containers);
# main also regressed joint ISO/IEC dispatch (relaton#239). Pin back —
# keys match relaton/cache/v2 — like standoc#1267.
gem "relaton", "= 3.0.0.pre.alpha.4"
gem "relaton-cli", github: "relaton/relaton", tag: "v3.0.0.pre.alpha.4", glob: "gems/relaton-cli/relaton-cli.gemspec" # keep in lockstep with the relaton pin above
gem "pubid", github: "pubid/pubid", branch: "main" # pubid#487 (5f3e9add73 polymorphic_name memo + alias folds) is on main; the perf/string-allocs branch is gone
# released relaton-render 1.3.0 still pulls the relaton-bib fragment, whose
# Relaton::RequestError redefinition clashes with the relaton monogem
# (superclass mismatch); render main depends on the monogem directly
gem "relaton-render" # 1.3 line: render main dropped Render::General (relaton-render#90) and
# 1.4.0.pre.alpha.2 is blocked by isodoc main's ~> 1.3.0 floor
