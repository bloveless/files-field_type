# Configuration

**Example Definition:**

```
protected $fields = [
    'example' => [
        'type'   => 'anomaly.field_type.files',
        'config' => [
            'disk'  => 'uploads',
            'path'  => 'Ryan Thompson/My Uploads',
            'image' => false,
            'mimes' => [
                'jpg',
                'xml'
            ],
            'max'   => 32
        ]
    ]
];
```

### `disk`

The disk to upload files to. Any valid disk slug or ID can be used. The default value is `'uploads'`.

### `path`

The upload path within the upload disk to upload files to. Any valid path string can be used. The default value is `null`.

If the path does not exist it will be created as needed.

### `image`

The "images only" flag. Enable to allow only images to be uploaded. The default value is `false`.

### `mimes`

The allowed file types that can be uploaded. Any array of valid file extensions can be used. The default value is `null` meaning any file type can be uploaded.

### `max`

The maximum file size allowed in megabytes. Any valid integer can be used. The default value is the server's maximum upload/post size.

If at any time the configured max becomes more than the server's max then the server's max will be used.
