docker_compose("./etc/docker/compose.yaml")

local_resource(
    'shopping-cart-service:local1',
    'mvn compile exec:exec -DAPP_CONFIG=local1.conf',
    dir='./shopping-cart-service',
    resource_deps=['kafka', 'db'],
    allow_parallel=True,
    auto_init=False,
    trigger_mode=TRIGGER_MODE_MANUAL
)

local_resource(
    'shopping-cart-service:local2',
    'mvn compile exec:exec -DAPP_CONFIG=local2.conf',
    dir='./shopping-cart-service',
    resource_deps=['kafka', 'db'],
    allow_parallel=True,
    auto_init=False,
    trigger_mode=TRIGGER_MODE_MANUAL
)

local_resource(
    'shopping-cart-service:local3',
    'mvn compile exec:exec -DAPP_CONFIG=local3.conf',
    dir='./shopping-cart-service',
    resource_deps=['kafka', 'db'],
    allow_parallel=True,
    auto_init=False,
    trigger_mode=TRIGGER_MODE_MANUAL
)