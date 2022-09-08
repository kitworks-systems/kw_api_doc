Developing endpoints
======================

Endpoint structure
------------------

.. code-block:: python

    @kw_api_route(route='/kw_api/auth/token/refresh', methods=['POST'], )
    @kw_api_wrapper(token=False, paginate=False, get_json=True, )
    def kw_api_auth_token_refresh_post(self, kw_api, **kw):
        token = kw_api.get_data_param_by_name('refreshToken', str)
        token = request.env['kw.api.token'].refresh_token_by_refresh_token(
            token)
        if token.is_refresh_token_expired:
            raise KwApiError(
                'auth_error', _('No token were given or given wrong one'),
                'refresh_token_expired')
        return kw_api.data_response(token.kw_api_get_data())


