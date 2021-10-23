package main

import (
	"encoding/json"
	"fmt"
)

type GetMeT struct {
	Ok     bool         `json: "ok"`
	Result GetMeResultT `json: "result"`
}

type GetMeResultT struct {
	Id        int64  `json: "id"`
	isBot     bool   `json: "is_bot"`
	FirstName string `json: "first_name"`
	Username  string `json: "username"`
}

func main() {
	getMeJson := `{
		"ok": true,
    	"result": {
			"id": 1164460711,
			"is_bot": true,
			"first_name": "Matrix",
			"username": "ShroudedAkaliBot",
			"can_join_groups": true,
			"can_read_all_group_messages": false,
			"supports_inline_queries": false
		}
	}`

	getMe := GetMeT{}

	err := json.Unmarshal([]byte(getMeJson), &getMe)
	if err != nil {
		fmt.Println(err.Error())

		return
	}

	fmt.Println(getMe)
}
