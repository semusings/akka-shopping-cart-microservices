local_resource(name='analytics:build', cmd='task analytics-service:build', allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
local_resource(name='cart:build', cmd='task cart-service:build', allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
local_resource(name='order:build', cmd='task order-service:build', allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

docker_compose("./etc/docker/compose.infra.yaml")
docker_compose("./etc/docker/compose.cart.yaml")

# local_resource(name='analytics:local1', serve_cmd='task analytics-service:exec-local1', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
# local_resource(name='analytics:local2', serve_cmd='task analytics-service:exec-local2', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
# local_resource(name='analytics:local3', serve_cmd='task analytics-service:exec-local3', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

# local_resource(name='cart:local1', serve_cmd='task cart-service:exec-local1', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
# local_resource(name='cart:local2', serve_cmd='task cart-service:exec-local2', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
# local_resource(name='cart:local3', serve_cmd='task cart-service:exec-local3', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

# local_resource(name='order:local1', serve_cmd='task order-service:exec-local1', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
# local_resource(name='order:local2', serve_cmd='task order-service:exec-local2', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
# local_resource(name='order:local3', serve_cmd='task order-service:exec-local3', resource_deps=['kafka', 'db'], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

