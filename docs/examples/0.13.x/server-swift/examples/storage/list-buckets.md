import Appwrite

func main() {
    let client = Client()
      .setEndpoint("https://[HOSTNAME_OR_IP]/v1") // Your API Endpoint
      .setProject("5df5acd0d48c2") // Your project ID
      .setKey("919c2d18fb5d4...a2ae413da83346ad2") // Your secret API key

    let storage = Storage(client)
    storage.listBuckets() { result in
        switch result {
        case .failure(let error):
            print(error.message)
        case .success(let bucketList):
            print(String(describing: bucketList)
        }
    }
}
