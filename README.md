# QAMc
# Video Upload Test Cases

## TC_VID_LEN_LOW1
**Title:** Verify if the video length stays within the boundary

**Test Type:** Boundaries

**Preconditions:**
- User account exists
- User is on login page
- User created a video

**Steps:**
1. User is logged in
2. Create a video that is 2 seconds long
3. Click post

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 67MB
- Length: 2 seconds
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- User gets a warning popup
- Warning message says video is too short make it longer
- Returns back to the editing

**Priority:** Low

---

## TC_VID_LEN_HIGH2
**Title:** Verify if the video length stays within the boundary

**Test Type:** Boundaries

**Preconditions:**
- User account exists
- User is on login page
- User created a video

**Steps:**
1. User is logged in
2. Create a video that is 10 minutes and 1 seconds long
3. Click post

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 67MB
- Length: 10 min 1 sec
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- User gets a warning popup
- Warning message says video is too long and need to be edited out
- Returns back to the editing

**Priority:** Low

---

## TC_FORMAT_NEG3
**Title:** Verify if the video is on the supported format

**Test Type:** Negative

**Preconditions:**
- User account exists
- User is on login page
- User created a video

**Steps:**
1. User is logged in
2. Create a video with MKV
3. Click post

**Test Data:**
- File: test_video.mkv
- Format: MKV
- Size: 67MB
- Length: 9
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- User gets a warning popup
- Warning message says video is recorded in the wrong format and tells the user to change it to mp4
- Returns back to the editing

**Priority:** High

---

## TC_ASPECT_NEG4
**Title:** Verify if the video's aspect ratio stays within the 9:16 range

**Test Type:** Negative

**Preconditions:**
- User account exists
- User is on login page
- User created a video

**Steps:**
1. User is logged in
2. Create a video in horizontal view
3. Click post

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 67MB
- Length: 9
- Resolution: 1080x1920
- Aspect Ratio: 12:16
- Caption: "Test upload"

**Expected:**
- User gets a warning popup
- Warning message says video's aspect ratio is messed up
- Returns back to the editing

**Priority:** Medium

---

## TC_VIDUPLOAD_5
**Title:** Verify that AVI formatted files upload seamlessly

**Test Type:** Positive

**Preconditions:**
- User account exists
- User is logged in
- User has created an AVI formatted video

**Steps:**
1. User clicks create/upload button
2. User selects a AVI formatted video
3. User attempts to upload video

**Test Data:**
- File: test_video.AVI
- Format: AVI
- Size: 67MB
- Length: 45 seconds
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- Upload is successful

**Priority:** High

---

## TC_VIDUPLOAD_6
**Title:** Verify that videos with a size of 256 upload seamlessly

**Test Type:** Positive

**Preconditions:**
- User account exists
- User is logged in
- User has created a video with a file size of 256MB

**Steps:**
1. User clicks create/upload button
2. User selects a video with a size of 256MB
3. User attempts to upload video

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 256MB
- Length: 45 seconds
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- Upload is successful

**Priority:** High

---

## TC_HASHMAX_7
**Title:** Verify that the hashtags under the video is less than or equal to 30

**Test Type:** Edge Cases

**Preconditions:**
- User account exists
- User is logged in
- User has created a video with a file size of 256MB
- User is inputting hashtags in the bottom of the video

**Steps:**
1. User clicks create/upload button
2. User selects a video with a size of 256MB
3. User selects 45 hashtags to add to the video
4. User attempts to upload video

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 256MB
- Length: 45 seconds
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- Upload is not successful and a warning popup
- The popup warns the user that they have inputted way too much hashtags and they have to take some out
- Brings the user back to the editing

**Priority:** Medium

---

## TC_CHARMAX_8
**Title:** Verify that the characters under the video is less than or equal to 2200

**Test Type:** Edge Cases

**Preconditions:**
- User account exists
- User is logged in
- User has created a video with a file size of 256MB
- User is inputting characters in the bottom of the video

**Steps:**
1. User clicks create/upload button
2. User selects a video with a size of 256MB
3. User selects 40000 characters to add to the video
4. User attempts to upload video

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 256MB
- Length: 45 seconds
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- Upload is not successful and a warning popup
- The popup warns the user that they have inputted way too much characters and they have to take some out
- Brings the user back to the editing

**Priority:** Medium

---

## TC_PUBLIC9
**Title:** Verify that the video the user posted is public

**Test Type:** Black Box

**Preconditions:**
- User account exists
- User is logged in
- User has created a video with a file size of 256MB
- User has posted a public video

**Steps:**
1. User clicks create/upload button
2. User selects a video with a size of 256MB
3. User selects public for video choice
4. User attempts to upload video

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 256MB
- Length: 45 seconds
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- Upload is successful
- Any user is able to open up TikTok and see the video even if they are not following

**Priority:** High

---

## TC_PUBLISH_10
**Title:** Verify that the publish button works

**Test Type:** Black Box

**Preconditions:**
- User account exists
- User is logged in
- User has a video to upload

**Steps:**
1. User clicks create/upload button
2. User selects a video
3. User attempts to upload video

**Test Data:**
- File: test_video.mp4
- Format: MP4
- Size: 256MB
- Length: 45 seconds
- Resolution: 1080x1920
- Aspect Ratio: 9:16
- Caption: "Test upload"

**Expected:**
- Upload is successful

**Priority:** High
