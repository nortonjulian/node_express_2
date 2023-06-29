Bug #1: /users route does not deny access if no token is provided.

Bug Fix:
The bug fix should have added authentication middleware to the /users route to ensure that access is denied if no token is provided.

Impact:
The existing test case in GET /users should now pass, as it expects a 401 status code when no token is provided.

Bug #2: /users/[username] route does not deny access if no token is provided.

Bug Fix:
The bug fix should have added authentication middleware to the /users/[username] route to ensure that access is denied if no token is provided.

Impact:
The existing test case in GET /users/[username] should now pass, as it expects a 401 status code when no token is provided.

Bug #3: /users/[username] route does not deny access if the user making the request is not an admin or the right user.

Bug Fix:
The bug fix should have updated the /users/[username] route to check if the user making the request is an admin or the right user before allowing access.

Impact:
The existing test case in PATCH /users/[username] should now pass, as it expects a 401 status code when the user making the request is not an admin or the right user.

Bug #4: /users/[username] route does not disallow patching not-allowed-fields.

Bug Fix:
The bug fix should have updated the /users/[username] route to disallow patching not-allowed-fields.

Impact:
The existing test case in PATCH /users/[username] should now pass, as it expects a 401 status code when trying to patch not-allowed-fields.

Bug #5: /users/[username] route does not return a 404 error if the user cannot be found.

Bug Fix:
The bug fix should have updated the /users/[username] route to return a 404 error if the
