# CURL playground
the cheatsheets of curl

# GET request
curl www.google.com
## GET with header
curl --header "Authorization: Bearer xxx" http://luz4-playaround.apps.openshift.aavn.local/luz_person/api/cities 	

# POST request
curl --request POST -u "admin:admin" "host:port/api/tokens"


curl --header "Authorization: Bearer eyJhbGciOiJSUzUxMiJ9.eyJzdWIiOiJhZG1pbiIsImNvbXBhbnktdGVuYW50Ijp7ImNvbXBhbnlJbmZvSWQiOjIsImNvbXBhbnlJZCI6MSwiY29tcGFueU5hbWUiOiJBbiBOYW0gR291cm1ldCBTw6BybCIsInN0YXR1cyI6IlRFU1RJTkciLCJzdGF0dXNFeHBpcnlEYXRlIjpudWxsLCJpZCI6NCwicm9sZXMiOlsiY29tcGFueV9hZG1pbmlzdHJhdG9yIiwiZW1wbG95ZWUiLCJleHRlcm5hbF91c2VyIl0sInRlbmFudElkIjoiMmQ5YTgxNWItNjgzOS00YjE5LWE5NGMtYzMwYzgxMDRkMjNlIiwidXNlcm5hbWUiOiIiLCJuYW1lIjpudWxsLCJ0eXBlIjoiQ09NUEFOWSIsImNyZWF0ZURhdGUiOm51bGwsImV4cGlyZURhdGUiOm51bGwsImV4cGlyZVRpbWUiOm51bGx9LCJpc3MiOiJjb20uYXhvbml2eSIsInVzZXJfcm9sZXMiOlsiRXZlcnlib2R5Iiwia2xhcmFfcm9sZXMiLCJBZG1pbmlzdHJhdG9yIiwiTmV3c19BZG1pbiIsImFsbF90ZW5hbnRzX2FjY2VzcyIsIlN1cHBvcnRlciJdLCJwZXJzb24tdGVuYW50Ijp7ImlkIjowLCJyb2xlcyI6W10sInRlbmFudElkIjoiMmQ5YTgxNWItNjgzOS00YjE5LWE5NGMtYzMwYzgxMDRkMjNlIiwidXNlcm5hbWUiOiJhZG1pbiIsIm5hbWUiOm51bGwsInR5cGUiOiJQRVJTT04iLCJjcmVhdGVEYXRlIjpudWxsLCJleHBpcmVEYXRlIjpudWxsLCJleHBpcmVUaW1lIjpudWxsfSwiZXhwIjoxNTU4MDk0ODU5LCJpYXQiOjE1NTgwOTMwNTl9.s2Hac8Y0oiej7zc_Q0oau1umEYCMOcTMHM6_ufHv3MV4PPqf6iXt_GoGGB5MLnww_iRNTMjKn2q5bf2ADxma1yQu7mM2KAuP7N9aLb1GlQ26TnZ-rw-E9ekNtrIhusAOf2_km3Jqx96Zk90yWS2FLUQEJHnGxDy_aPNw0MWZNAQnsuu5TTxf0NZx_AkFRANNwpjx1Odznr67b70zikYNvCT-uOUf342esXfI0mDt_BXpspeKP-u02mXv5022aVVMNydQwzZsiXfxOvjdO3HDrLISEEJ8j7SbZkZJF5P7XH0RFa-kKmN-tJqUxPBHx7m6m_iE_P9DyCXWfwyYzqu2cQ" http://host:port/project_context/api/...

curl --header "Authorization: Bearer eyJhbGciOiJSUzUxMiJ9.eyJzdWIiOiJhZG1pbiIsImNvbXBhbnktdGVuYW50Ijp7ImNvbXBhbnlJbmZvSWQiOjIsImNvbXBhbnlJZCI6MSwiY29tcGFueU5hbWUiOiJBbiBOYW0gR291cm1ldCBTw6BybCIsInN0YXR1cyI6IlRFU1RJTkciLCJzdGF0dXNFeHBpcnlEYXRlIjpudWxsLCJpZCI6NCwicm9sZXMiOlsiY29tcGFueV9hZG1pbmlzdHJhdG9yIiwiZW1wbG95ZWUiLCJleHRlcm5hbF91c2VyIl0sInRlbmFudElkIjoiMmQ5YTgxNWItNjgzOS00YjE5LWE5NGMtYzMwYzgxMDRkMjNlIiwidXNlcm5hbWUiOiIiLCJuYW1lIjpudWxsLCJ0eXBlIjoiQ09NUEFOWSIsImNyZWF0ZURhdGUiOm51bGwsImV4cGlyZURhdGUiOm51bGwsImV4cGlyZVRpbWUiOm51bGx9LCJpc3MiOiJjb20uYXhvbml2eSIsInVzZXJfcm9sZXMiOlsiRXZlcnlib2R5Iiwia2xhcmFfcm9sZXMiLCJBZG1pbmlzdHJhdG9yIiwiTmV3c19BZG1pbiIsImFsbF90ZW5hbnRzX2FjY2VzcyIsIlN1cHBvcnRlciJdLCJwZXJzb24tdGVuYW50Ijp7ImlkIjowLCJyb2xlcyI6W10sInRlbmFudElkIjoiMmQ5YTgxNWItNjgzOS00YjE5LWE5NGMtYzMwYzgxMDRkMjNlIiwidXNlcm5hbWUiOiJhZG1pbiIsIm5hbWUiOm51bGwsInR5cGUiOiJQRVJTT04iLCJjcmVhdGVEYXRlIjpudWxsLCJleHBpcmVEYXRlIjpudWxsLCJleHBpcmVUaW1lIjpudWxsfSwiZXhwIjoxNTU4MDk0ODU5LCJpYXQiOjE1NTgwOTMwNTl9.s2Hac8Y0oiej7zc_Q0oau1umEYCMOcTMHM6_ufHv3MV4PPqf6iXt_GoGGB5MLnww_iRNTMjKn2q5bf2ADxma1yQu7mM2KAuP7N9aLb1GlQ26TnZ-rw-E9ekNtrIhusAOf2_km3Jqx96Zk90yWS2FLUQEJHnGxDy_aPNw0MWZNAQnsuu5TTxf0NZx_AkFRANNwpjx1Odznr67b70zikYNvCT-uOUf342esXfI0mDt_BXpspeKP-u02mXv5022aVVMNydQwzZsiXfxOvjdO3HDrLISEEJ8j7SbZkZJF5P7XH0RFa-kKmN-tJqUxPBHx7m6m_iE_P9DyCXWfwyYzqu2cQ" http://host:port/project_context/api/...


curl --request POST -H "Content-Type:multipart/form-data" \
	-F LUZ_USERNAME="smurfs" \
	-F LUZ_PASSWORD="admin" \
	-F LUZ_TOKEN_HOST="http://localhost:8081/" \
	-F LUZ_COMPENSATION_HOST="http://localhost:8081/" \
	-F LUZ_PERSON_HOST="http://localhost:8081/" \
	-F file=@"C:\work\opt\workspace\workspaceSmurfs\luzcomp_scripts\src\main\resources\com\axonivy\swissdec\standard_configuration.groovy" \
	-u "admin:admin" \
	"localhost:8081/luz_scripting_web/api/execute-groovy-script"


curl --request POST --header "Content-Type:multipart/form-data" \
	-F LUZ_USERNAME="smurfs" \
	-F LUZ_PASSWORD="admin" \
	-F LUZ_TOKEN_HOST="http://localhost:8080/" \
	-F LUZ_COMPENSATION_HOST="http://localhost:8080/" \
	-F LUZ_PERSON_HOST="http://localhost:8080/" \
	-F file=@"C:\work\opt\workspace\workspaceSmurfs\luzcomp_scripts\src\main\resources\com\axonivy\swissdec\standard_configuration.groovy" \
	-u "admin:admin" \
	"host:port/project_context/api/execute-groovy-script"


curl --request POST -u "admin:admin" "host:port/project_context/api/..."
