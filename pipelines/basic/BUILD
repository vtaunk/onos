COMPILE_DEPS = CORE_DEPS + [
    "@minimal_json//jar",
    "//drivers/default:onos-drivers-default",
    "//protocols/p4runtime/model:onos-protocols-p4runtime-model",
    "//protocols/p4runtime/api:onos-protocols-p4runtime-api",
    "//apps/inbandtelemetry/api:onos-apps-inbandtelemetry-api",
]

BUNDLES = [
    "//pipelines/basic:onos-pipelines-basic",
    "//apps/inbandtelemetry/api:onos-apps-inbandtelemetry-api",
]

osgi_jar(
    deps = COMPILE_DEPS,
)

onos_app(
    app_name = "org.onosproject.pipelines.basic",
    category = "Pipeline",
    description = "Provides pipelines with basic L2/L3 forwarding capabilities and packet-in/out " +
                  "support.",
    included_bundles = BUNDLES,
    required_apps = [
        "org.onosproject.drivers.p4runtime",
    ],
    title = "Basic Pipelines",
    url = "http://onosproject.org",
)
